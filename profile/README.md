## Welcome to the **Vault Web GitHub Organization** 👋

Our mission is to build a **modular, self-hosted home portal ecosystem** that allows users to manage their **private services securely from a single dashboard**.  
Vault Web aims to provide a **central entry point for multiple tools**—from file management to chats and future services—**optimized for home server environments**.

The organization is designed as a **learning- and experimentation-focused ecosystem**, combining clean architecture with real-world use cases around authentication, distributed services, and self-hosting.

---

## Architecture Overview

Vault Web follows a clear and intentional architecture:

- 🧱 **One core monolithic application** (Vault Web)
- 🔌 **Multiple independent backend services**
- 🖥️ **One centralized frontend** that integrates all services via APIs

### Key Principles

- All backend services live in **separate repositories**
- The **entire frontend is centralized** in the core Vault Web repository
- External services run **fully independently**
- Communication happens **only via APIs**
- If one service fails, the rest of the system continues to work
- New services can be added **without modifying existing backends**

This keeps the system extensible without unnecessary coupling.

---

## Our Projects

### 1. [Vault Web (Core)](https://github.com/Vault-Web/vault-web)

The heart of the ecosystem and the main user entry point.

**Tech stack**
- Spring Boot (backend)
- Angular (frontend)
- PostgreSQL (database)

**Responsibilities**
- 💬 Internal chats and basic collaboration tools  
- 🧑‍💻 User and session management  
- 🔐 Central login & JWT handling  
- 🖥️ Unified dashboard UI  
- 🧩 Frontend integration of all external services  

⚠️ The Vault Web backend handles **core services only**.  
All other services are accessed via APIs and do **not** depend on it.

---

### 2. [Cloud Page](https://github.com/Vault-Web/cloud-page)

A **backend-only**, fully independent service for file and folder management.

**Features**
- File explorer–style API
- View, create, edit, and delete files and folders
- Per-user file isolation
- JWT-based authentication

Cloud Page runs standalone and is integrated into the Vault Web frontend via API calls.

---

### 3. [Auth API Gateway](https://github.com/Vault-Web/auth-api-gateway)

An important architectural improvement currently under active development.

**Goal**
Introduce a **central authentication & authorization gateway**.

Instead of each service validating JWTs individually, the gateway will:
- handle authentication
- validate tokens
- enforce authorization rules

This will simplify backend services, improve security consistency, and make the ecosystem easier to extend.

Contributions and design discussions are **highly welcome**.

---

### 4. [Password Manager](https://github.com/Vault-Web/password-manager)

A future backend service focused on secure password management.

**Status**
- Currently in research and planning phase
- Strong focus on encryption, secure storage, and threat modeling

Because of the sensitive security domain, development is intentionally cautious.
Conceptual and security-focused contributions are especially valuable.

---

### 5. [Server Docs](https://github.com/Vault-Web/server-docs)

The central documentation repository for the entire ecosystem.

Includes:
- Detailed documentation for all Vault Web services
- Example home server deployments
- Headscale VPN integration
- Best practices for self-hosting

---

## Goals & Philosophy

- **Modularity**: Services can be developed, replaced, or extended independently  
- **Home-server focus**: Built for self-hosted environments and hands-on learning  
- **Clean architecture**: Clear separation between core, services, and frontend  
- **Continuous improvement**: Active development and architectural evolution  

---

## How to Get Involved

We welcome:
- bug reports
- architectural discussions
- new service ideas
- code contributions

Please follow the contribution guidelines:  
👉 https://github.com/Vault-Web/.github/blob/main/CONTRIBUTING.md

You can also open Issues or start Discussions in any repository.

---

💡 **Note**  
Vault Web is primarily designed for **home-server experimentation and learning**.  
While functional, it should not be considered production-ready without proper security review and hardening.
