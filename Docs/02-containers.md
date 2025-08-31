# Diagrama de Containers

```mermaid
C4Container
    title Sistema de Excursões – Diagrama de Containers
    Person(cliente, "Cliente")
    Person(empresa, "Empresa de Excursões")

    System_Boundary(sistema, "Plataforma de Excursões") {
        Container(web, "Web App", "React/Next.js", "Interface para clientes e empresas")
        Container(app, "Mobile App", "Flutter/React Native", "App para clientes e empresas")
        Container(api, "API Backend", ".NET 8 + Clean Architecture", "Orquestra lógica de negócio")
        ContainerDb(db, "Database", "PostgreSQL", "Armazena dados do sistema")
    }

    cliente -> web : Usa
    cliente -> app : Usa
    empresa -> web : Usa
    empresa -> app : Usa

    web -> api : Consome
    app -> api : Consome
    api -> db : CRUD
    api -> pgto : Integração
    System_Ext(pgto, "Gateway de Pagamentos")
```