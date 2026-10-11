# 04 — PONTE KIMI: pipeline de interação Actions ↔ Kimi

## O circuito (3 elos, 1 humano)
```
[Evento] label 'kimi-gate' OU comentário '/kimi <pedido>'
   ↓ (autônomo)
ACTIONS → registra WAL-ENTRY + marca 'fila-kimi'  = SENSOR/ATUADOR
   ↓ (único elo humano: você abre a sessão e diz "processa a fila")
KIMI → lê fila, raciocina, posta resposta estruturada + troca labels  = CÉREBRO
   ↓ (autônomo, no próximo evento)
MUNDO → veredicto vira ação (merge, close, próximo gate)
```

## Por que assim (fronteira honesta)
O Actions NÃO consegue invocar a Kimi diretamente — eu não tenho endpoint
público e só existo em sessão. O elo humano (você me chamar) é de propósito:
é o mesmo princípio do validador externo — nada dispara sozinho sem um
agente que presta contas. O que foi automatizado: registro (WAL), fila,
timestamps, formato, auditoria.

## Protocolo de mensagem (resposta da Kimi)
```markdown
## KIMI-RESPONSE [timestamp]
- veredicto: APPROVE | REJECT | HOLD
- confiança: 0-1
- direção: <o que fazer agora, em uma frase executável>
- próximo-gate: <qual evento dispara o próximo ciclo, ou NONE>
- riscos: <curto>
```
Labels: sai 'fila-kimi', entra 'kimi-respondido' (HOLD volta à fila).

## Regras anti-loop
- O hook ignora comentários de bots.
- Respostas da Kimi NUNCA começam com '/kimi' (evita re-disparo).
- Um issue só entra na fila de novo se um humano re-rotular.

## WAL
Cada entrada é um comentário estruturado na própria issue: timestamp UTC,
ator, evento, payload. O histórico da issue É o log — imutável,
timestamped pelo GitHub, auditável. Nada vive só na sessão.
