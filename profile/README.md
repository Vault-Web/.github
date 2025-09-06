## Welcome to the **Vault Web GitHub organization**!

Our mission is to build a **modular, self-hosted home portal ecosystem** that allows users to manage their own private services securely from a single dashboard. The goal is to provide a **central entry point for multiple tools**—from file storage to chats and much more—optimized for home server environments.

---

## Our Projects

### 1. [Vault Web](https://github.com/Vault-Web/vault-web)
The core of the ecosystem.  
- Full-stack project with **Spring Boot backend**, **Angular frontend**, and **PostgreSQL** database.  
- Provides:
  - 💬 **Internal chats and collaboration tools**  
  - ☁️ **Private file cloud** (`vault-cloud`) for secure storage  
  - 🔐 **Built-in password manager**  
  - 🧑‍💻 **User and session management**  
- Designed to be **modular and extensible**, perfect for experimenting with home server features.  

### 2. [Cloud Page](https://github.com/Vault-Web/cloud-page)
A dedicated backend service for managing files and folders for each user.  
- Provides a **file explorer-like interface** via API.  
- Allows **viewing, creating, editing, and deleting files** associated with each account.  
- Authenticated with **JWT tokens**, sharing the same master key as Vault Web.  
- Focused on **private, home-server storage** with secure access.  

### 3. [Password Manager](https://github.com/Vault-Web/password-manager)
Planned future project.  
- Will provide a **secure, self-hosted password management tool**.  
- Currently under research for **security feasibility and best practices**.  

### 4. [Server Docs](https://github.com/Vault-Web/server-docs)
Central documentation repository.  
- Contains **detailed documentation for all Vault Web repositories**.  
- Includes a **sample server setup** on [Deniz’s](https://github.com/DenizAltunkapan) server with **Headscale VPN** integration.  
- Provides step-by-step instructions, best practices, and usage examples.

---

## Goals & Philosophy

- **Modularity**: Each service can be **developed, replaced, or extended independently**.  
- **Home-server focus**: Designed for self-hosted environments, allowing hands-on learning and experimentation.  
- **Continuous improvement**: Projects are under **active development** and evolve with new features.  

---

## How to Get Involved

We welcome contributions, suggestions, and bug reports. Please follow the [contribution guidelines](https://github.com/Vault-Web/.github/blob/main/CONTRIBUTING.md).  

---

💡 **Note:** This organization is primarily for **home-server experimentation**. Services are functional, but care should be taken before using them in production environments.
