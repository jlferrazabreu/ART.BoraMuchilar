# Plataforma de Turismo Rodoviário – Arquitetura

Este repositório contém os diagramas arquiteturais da solução de turismo rodoviário (modelo de negócio **B2B2C**).  
A plataforma atende **turistas, excursionistas, empresas parceiras e guias**, permitindo **gestão de excursões, reservas, pagamentos e check-in via QR Code**.

---

## 📐 Diagramas Arquiteturais

### 1. Contexto (C4 – Nível 1)
Visão de alto nível dos **atores externos**, da **plataforma** e suas **integrações**.  
👉 [Ver diagrama](01-contexto.md)

### 2. Containers (C4 – Nível 2)
Mostra os principais blocos da solução (**frontends, backend modular, integrações e infraestrutura**).  
👉 [Ver diagrama](02-containers.md)

### 3. Componentes (C4 – Nível 3 – Booking & Payments)
Foco no fluxo de **reserva e pagamento**, detalhando **controllers, application layer e domain models**.  
👉 [Ver diagrama](03-componentes-booking-payments.md)

### 4. Sequência – Reserva e Pagamento
Exemplo de fluxo crítico: do **hold da reserva** até a **confirmação e emissão de voucher/QR**.  
👉 [Ver diagrama](04-sequencia-booking-payment.md)

### 5. Diagrama de Classes – Módulo Catalog
Detalhamento do domínio **Catalog**, incluindo **Excursion, Departure, Itinerary, Pricing, SeatMap e Allotment**.  
👉 [Ver diagrama](05-catalog-classdiagram.md)

---

## 🛠️ Tecnologias e Stack Proposta
- **Backend**: .NET 8 (ASP.NET Core, Clean Architecture)
- **Frontend Web**: Next.js + Tailwind
- **Mobile**: React Native
- **Banco de Dados**: PostgreSQL (multi-tenant)
- **Mensageria/Eventos**: RabbitMQ ou Kafka
- **Cache**: Redis
- **Auth**: Keycloak/Auth0
- **Infra**: Docker, Kubernetes, GitHub Actions (CI/CD)

---

✍️ Documento inicial de arquitetura – sujeito a evoluções conforme backlog e roadmap do produto.
