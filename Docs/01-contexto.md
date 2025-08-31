# Diagrama de Contexto

```mermaid
C4Context
    title Sistema de Excursões – Diagrama de Contexto
    Person(cliente, "Cliente", "Pessoa interessada em excursões")
    Person(empresa, "Empresa de Excursões", "Dono/gestor de empresa parceira")
    System(sistema, "Plataforma de Excursões", "Centraliza excursões, passageiros e pagamentos")

    cliente -> sistema : Compra excursões, acompanha status e roteiros
    empresa -> sistema : Gerencia excursões, passageiros e pagamentos
    System_Ext(pgto, "Gateway de Pagamentos", "Processa transações financeiras")
    sistema -> pgto : Solicita processamento de pagamento
```