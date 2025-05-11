# 🏦 BankApplication - Microservicios con Spring Boot

Este proyecto es una aplicación bancaria distribuida en microservicios construida con **Spring Boot**. Implementa operaciones CRUD para clientes, cuentas y transacciones, además de lógica de negocio para registrar movimientos y generar reportes por cliente y fecha.

## 📦 Estructura del Proyecto

```
BankApplication/
├── client/           # Microservicio de Clientes
├── account/          # Microservicio de Cuentas y Transacciones
├── collection_bank_postman.json
└── README.md
```

## 🔧 Tecnologías utilizadas

- Java 11+
- Spring Boot
- Spring Data JPA
- H2 (para pruebas)
- Maven
- Postman (colección incluida)
- JUnit 5 + Mockito

---

## 🚀 Microservicios

### 📁 client (puerto 8001)

Gestiona entidades:
- `Person` (superclase)
- `Client` (hereda de Person)

### 📁 account (puerto 8000)

Gestiona:
- `Account` (cuenta bancaria)
- `Transaction` (movimientos de cuenta)

Comunicación esperada: asíncrona entre servicios (simulada en esta versión)

---

## 🔌 Endpoints principales

### Clientes (`/api/clients`)
- `GET /api/clients`
- `GET /api/clients/{id}`
- `POST /api/clients`
- `PUT /api/clients/{id}`
- `PATCH /api/clients/{id}`
- `DELETE /api/clients/{id}`

### Cuentas (`/api/accounts`)
- `GET /api/accounts`
- `POST /api/accounts`
- ...

### Transacciones (`/api/transactions`)
- `POST /api/transactions`
- `GET /api/transactions`
- `GET /api/transacciones/clients/{clientId}/report?dateTransactionStart=...&dateTransactionEnd=...`

---

## 🧪 Pruebas

### Prueba Unitaria (`F5`)
- `sampleTest.java`: valida el método `create` de ClientController

### Prueba de Integración Simulada (`F6`)
- `integrationSimulation()`: simula flujo completo de cliente, cuenta y transacción

---

## 🧾 Colección Postman

Incluida en:  
📄 `collection_bank_postman.json`

Permite probar fácilmente todos los endpoints definidos con datos reales (cliente: Eduardo, cuenta: 123456789).

---

## 📌 Autor

**Eduardo García Castro**  
Especialista en Backend · Java · Spring Boot · SQL
