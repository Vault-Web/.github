# Vault Web

**Vault Web** is the core project of the **Vault Web ecosystem**.  
It is a full-stack application combining a **Spring Boot backend**, an **Angular frontend**, and a **PostgreSQL** database.

Vault Web acts as a **central dashboard** for a modular, self-hosted home server ecosystem. It provides a single entry point where multiple services are integrated into one secure web interface.

---

## What Vault Web Provides

Vault Web is responsible for:

- 💬 **Internal chats and collaboration tools**
- 🧑‍💻 **User and session management**
- 🔐 **Central authentication (JWT-based)**
- 🧩 **Frontend integration of external services**

Additional services are **not implemented directly in this repository**, but are embedded into the Vault Web frontend.

For example, file storage and file management are provided by the **Cloud Page** service:  
👉 https://github.com/Vault-Web/cloud-page

---

## Project Structure

- 📁 [**DIRECTORY.md**](https://github.com/Vault-Web/vault-web/blob/main/DIRECTORY.md) – generated project structure overview  
- 📚 [**Javadoc**](https://vault-web.github.io/vault-web) – backend API documentation  

---

## Local Development

Vault Web uses **Docker** for local development.

### Requirements

- Docker & Docker Compose  
- Java 21+ (Java 24 supported)  
- Node.js & npm  

---

## 1. Clone the Repository

```bash
git clone https://github.com/Vault-Web/vault-web.git
cd vault-web
````

---

## 2. Environment Configuration (`.env`)

⚠️ **You do NOT need to create a `.env` file manually.**
A `.env` file already exists in the repository.

You may adjust the values if needed, but make sure that:

> **The database configuration in `.env` matches exactly with the backend `application.properties`.**

---

## 3. Start PostgreSQL and pgAdmin

```bash
docker compose up -d
```

* PostgreSQL: `localhost:<DB_PORT>`
* pgAdmin: [http://localhost:8081](http://localhost:8081)

---

## 4. Backend (Spring Boot)

Configuration file:
`backend/src/main/resources/application.properties`

Ensure the database values match the `.env` file.

Start the backend:

```bash
cd backend
./mvnw spring-boot:run
```

* API: [http://localhost:8080](http://localhost:8080)
* Swagger UI: [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

---

## 5. Frontend (Angular)

```bash
cd frontend
npm install
ng serve
```

Open:
👉 [http://localhost:4200](http://localhost:4200)

---

## Notes

This project is intended for **self-hosted and home-server environments**.
Contributions and feedback are welcome.
