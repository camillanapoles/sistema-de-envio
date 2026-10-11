# 05 — GOVERNANÇA: correções estruturais dos erros diagnosticados
Codificação em regra dos achados do diagnóstico causal (2026-10-11).
Estas regras valem para TODO projeto neste repositório e qualquer sistema futuro.

## ERRO 1 — Morte no pós-aprovação (contrato aprovado → nunca validado)
CORREÇÃO: Delivery Gate mecânico.
- Nenhum projeto novo inicia enquanto existir artefato não-enviado (WIP = 1).
- "Done" = confirmação EXTERNA registrada, nunca autoavaliação.
- Contrato sem validador nomeado (campo 5) é INCOMPLETO e não inicia.

## ERRO 2 — Persistência invertida (ideia eterna, artefato descartável)
CORREÇÃO: Contrato de sobrevivência do artefato.
- Artefato só existe se tiver endereço fora de qualquer sessão de IA.
- Regra prática: se o link não abre no navegador anônimo, não existe.
- Este repositório é a casa oficial; sessões são oficinas, nunca o depósito.

## ERRO 3 — Ausência de juiz externo
CORREÇÃO: Validação em dois níveis, gate congelado.
- NÍVEL 1 (autônomo, CI/CD): gate objetivo definido ANTES da construção,
  executado a cada push. Falha = REJECT automático + issue /kimi (diagnóstico
  entra na fila com bundling de correção obrigatório).
- NÍVEL 2 (exposição): link público permanente — mínimo inegociável.
- CLÁUSULA ANTI-CIRCUNVENÇÃO: gate congelado após aprovação do contrato.
  Alterá-lo exige entrada WAL + re-aprovação. Gate editável livremente =
  validação maleável = o ERRO 3 de volta com roupas novas.
- Auto-nota (PQMS próprio) continua formalmente INVÁLIDA como done.

## ERRO 4 — Meta-evitação (sistemas-meta como fuga do trabalho-objeto)
CORREÇÃO: Regra da bootstrap concreta.
- Sistema-meta só pode existir carregando um artefato-objeto com envio ≤ 30 dias.
- Proibição de novo sistema-meta até 3 artefatos-objeto validados externamente.
- Teste de falsificabilidade: se o "sistema" não pode falhar, ele é evitação — reescrever até poder falhar.

## ERRO 5 — Diagnóstico sem correção (Grupo B: insight registrado, fix nunca)
CORREÇÃO: Bundling obrigatório.
- Diagnóstico só é registrado com correção mínima agendada na MESMA sessão.
- Agente sem artefato verificável não está "documentado": está "lembrado".
  (Este repositório é a prova: 6 agentes em EM MEMÓRIA = fila de correções, não acervo.)

## ERRO 6 — Métrica que não cobra entrega
CORREÇÃO: Placar único.
- Métrica oficial: ARTEFATOS EXISTENTES FORA DO MEU CONTROLE, POR TRIMESTRE.
- Conteúdo de 01-PORTFOLIO-REAL.md, seção ENVIADOS, é a fonte da métrica.
- Sofisticação de especificação vale ZERO pontos neste placar.

## Protocolo de funeral
Projeto sem avanço por 30 dias NÃO é abandonado: é decidido. Registrar em
MORTOS DECIDIDOS com motivo. Limbo (nem vivo nem morte decidida) é proibido.

## Regra do robô
O Cobrador (segunda 07h) e o Gate Hook (/kimi ou label kimi-gate) operam
acima destas regras: são a camada de enforcement, não dependem de memória
ou boa vontade.
