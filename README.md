# qa-dados
  Esta query consolida, em uma única linha por pessoa (person_id), informações completas sobre a última compra registrada de cada usuário no ambiente prod_lake_ss_refined do Data Lake Smart Fit.
  
  O objetivo é gerar uma visão unificada que combine dados de purchases, pagamentos, reembolsos, acessos, convidados e status de relacionamento com a academia, mantendo coerência temporal e integridade relacional.

⚙️ Principais Objetivos

  Retornar a última compra (last_purchase) de cada pessoa com base em created_at e id.
  
  Consolidar dados de múltiplas fontes (payments, refunds, memberships, wallets, etc.) em uma única visão normalizada.
  
  Identificar:
  
  - Status da matrícula (ativo / cancelado)
  - Status do cliente (active / inactive)
  - Situação do documento de pagamento (positivo / negativo)
  - Presença de reembolso/abono (abono)
  - Indicador de recompra (rebuy)
  - Quantidade de acessos e convites
  - Volume e valor de pagamentos (payed, scheduled, rejected)


⚡ Resultados Esperados

- 1 linha por pessoa (person_id)
- Dados consistentes e não duplicados
- Integração entre status de pagamento, engajamento e matrícula
