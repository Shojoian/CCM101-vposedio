# 🏗️ Multi-Tier Application Architecture

## Overview: What is a Two-Tier Architecture?
A **Two-Tier Architecture** is a software design pattern that divides an enterprise application into two logically and physically isolated layers: the **Web/Application Tier** (frontend presentation and business logic) and the **Database Tier** (backend persistent data storage). In a containerized cloud environment, each tier runs inside its own dedicated container and communicates securely over a private virtual network.

---

## 🖥️ 1. The Web/Application Tier (`Nextcloud`)
* **Primary Role:** Serves as the frontend presentation layer and core application engine that users interact with directly through their web browsers or mobile clients.
* **Key Responsibilities:**
  * Handles incoming HTTP/HTTPS requests on exposed network ports (such as Port `8080` mapped to internal Port `80`).
  * Renders the graphical user interface (GUI), file upload dashboards, and sharing menus.
  * Executes application logic, authenticates user sessions, and translates user actions into structured queries sent to the backend database.

---

## 🗄️ 2. The Database Tier (`MariaDB`)
* **Primary Role:** Acts as the dedicated backend relational database management system (RDBMS) responsible for storing, indexing, and protecting structured information.
* **Key Responsibilities:**
  * Persists critical metadata, including user account credentials, access permissions, folder hierarchies, and file sharing links.
  * Processes SQL queries requested by the Nextcloud application tier with high concurrency and transactional integrity.
  * Remains isolated from public internet traffic, accepting connections strictly from authorized internal application containers.

---

## 🔗 3. Why Separate Them?
Separating the web server and the database into two distinct containers adheres to the cloud-native principle of **single responsibility and decoupling**, allowing each tier to be scaled, updated, or restarted independently without taking down the entire system. If both services were packed into a single container, a spike in web traffic or a routine web server update would risk corrupting database transactions and force unnecessary downtime for the database. Furthermore, isolating the database in its own container significantly improves security by ensuring the database engine is never directly exposed to public network ports.
