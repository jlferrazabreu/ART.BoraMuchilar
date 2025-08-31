# Diagrama de Componentes – Booking & Payments

```mermaid
C4Component
    title Módulo Booking & Payments
    Container(api, "API Backend", ".NET 8")

    Component(bookingSvc, "Booking Service", "Gerencia reservas de excursões")
    Component(paymentSvc, "Payment Service", "Orquestra pagamentos")
    Component(notificationSvc, "Notification Service", "Envia e-mails/avisos de status")

    api -> bookingSvc
    api -> paymentSvc
    bookingSvc -> paymentSvc : Solicita cobrança
    paymentSvc -> notificationSvc : Notifica sucesso/erro
    Component_Ext(pgto, "Gateway de Pagamentos")
    paymentSvc -> pgto
```