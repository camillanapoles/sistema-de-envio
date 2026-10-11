# CONTRATO DE ENVIO — template obrigatório

REGRA: nenhum projeto pode ser iniciado sem este contrato completo.
REGRA: campos 5 e 7 NÃO podem ser preenchidos por você sozinha(o).

---

## 1. Nome do projeto
## 2. Problema real que resolve (uma frase, para um humano entender)
## 3. MÍNIMO ENVIÁVEL (o menor artefato que já é útil para alguém)
   — se não couber em 2 semanas de trabalho, cortar até caber
## 4. FORA DE ESCOPO (o que este projeto NÃO faz — proteção contra expansão)
## 5. VALIDADOR (escolher UM, definir ANTES da construção):
   OPCAO A — GATE CI: workflow validador.yml com checagens objetivas listadas aqui.
             Gate é CONGELADO após aprovação. Falha = REJECT automático + issue /kimi.
             Alterar o gate exige entrada WAL em 06-DIARIO-CORRECAO.md + re-aprovação.
   OPCAO B — PESSOA REAL: nome + data combinada para leitura/uso.
   Sem um dos dois, o projeto NÃO começa.
## 6. ENDEREÇO DE PERSISTÊNCIA: onde o artefato vive, fora de qualquer sessão de IA
   — GitHub: ____________   Drive: ____________   outro: ____________
   — quem acessa sem mim e sem a IA: ____________
## 7. DATA DE ENVIO (fixa, ≤ 30 dias da assinatura): __/__/____
## 8. SE não enviar até a data: funeral explícito (decidir morte, não omissão)
## 9. Assinatura + data

---
Anti-padrões detectados no histórico (checklist de não-repetição):
[ ] escopo aberto          [ ] validação maleável       [ ] artefato só na sessão
[ ] recomeço com projeto novo antes de enviar este
NOTA: gate CI que você pode editar livremente depois = validação maleável.
      O gate congelado é o que o transforma em juiz, não em espelho.

## 5b. VALIDADOR: ____ (quebrado propositalmente para teste)
