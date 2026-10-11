# 07 — BOOTSTRAP DE SESSÃO (cold start)
Protocolo de retomada para QUALQUER sessão nova — humana ou IA.
Princípio: a sessão não lembra de nada; o REPOSITÓRIO é a memória.

## Passo 1 — [HUMANO] Abrir a sessão e fornecer acesso
Cole o token (ou crie um novo em github.com/settings/tokens, scope: repo) e diga: **"boot"**.

## Passo 2 — [KIMI] Executar a leitura fria (nesta ordem)
1. `01-PORTFOLIO-REAL.md` → reportar: EM VOO, FILA, ENVIADOS, MORTOS
2. `06-DIARIO-CORRECAO.md` → reportar: pendências com dono
3. Issues abertas → cobranças sem resposta, fila-kimi aguardando
4. Última run do Cobrador e do Auditor (aba Actions)

## Passo 3 — [KIMI] Pergunta obrigatória (portão de envio)
Reportar e perguntar: **"envio, mato ou continuo?"**
- CONTINUO = avanço concreto neste turno (artefato tocado, nunca re-arquitetura)
- ENVIO = mover para validador e fechar ciclo
- MATO = funeral explícito em MORTOS DECIDIDOS com motivo

## Passo 4 — Proibições automáticas
- Proibido propor projeto novo se EM VOO estiver ocupado
- Proibido registrar diagnóstico sem correção mínima agendada
- Proibido "done" sem confirmação externa (regra 05)

## Exemplo de saída de boot (válido em qualquer data)
> "Boot ok. Em voo: CATALOGO-AGENTES-SDK v1.0 (envio proposto 25/10, validador pendente).
> Pendências: [você] nomear validador; [você] revogar token; [sistema] cobrança seg 07h.
> Issues: 1 auditoria aberta. Pergunta: envio, mato ou continuo?"
