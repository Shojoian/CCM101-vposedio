# 🚀 Laboratory 6: The Cloud Deployment Engineer

Welcome to the official documentation for **Laboratory 6: The Cloud Deployment Engineer**. This repository entry documents the transition from manual single-container CLI operations to automated multi-tier **Infrastructure as Code (IaC)** deployments using **Docker Compose**, **Nextcloud**, and **MariaDB**.

---

## 🌐 Mission Overview
As part of the Cloud Deployment Team at CloudNova Technologies, this mission delivers a self-hosted, enterprise-grade private cloud storage proof-of-concept for a university client migrating away from third-party commercial storage. 

Because production web applications require persistent relational databases to store user accounts and file metadata, this laboratory implements a decoupled **Two-Tier Architecture**. Using a declarative `docker-compose.yml` configuration file, both a backend **MariaDB** database tier and a frontend **Nextcloud** application tier were orchestrated, networked, verified, and managed simultaneously with single-command precision.

---

## 🎯 Mission Objectives
* 🏗️ **Multi-Tier Architecture Analysis:** Explain the operational responsibilities and security benefits of separating the Web/Application Tier from the Database Tier.
* 📄 **Infrastructure as Code (IaC) Design:** Understand the syntax, indentation rules, and declarative structure of a `docker-compose.yml` configuration file.
* ⌨️ **CLI Configuration Authoring:** Utilize the Linux `nano` text editor to construct a multi-service YAML deployment blueprint.
* 🐳 **Multi-Container Orchestration:** Deploy, verify, and tear down an interconnected Nextcloud and MariaDB stack using Docker Compose.
* 📝 **Technical Documentation:** Author comprehensive Markdown documentation detailing service discovery, YAML orchestration, and IaC principles in a structured GitHub portfolio.

---

## 💻 Commands Executed
* `mkdir nextcloud-deployment && cd nextcloud-deployment` - Created and entered the dedicated working directory for the Docker Compose stack.
* `nano docker-compose.yml` - Opened the terminal text editor to write the declarative YAML configuration for the `database` (`mariadb:10.6`) and `app` (`nextcloud`) services.
* `docker-compose up -d` - Parsed the YAML blueprint, created a shared bridge network, pulled both container images, and launched the multi-container stack in detached mode.
* `docker-compose ps` - Inspected the operational status and port bindings of all containers belonging to the Compose stack.
* `docker-compose down` - Gracefully stopped all running containers in the stack and removed the containers and default virtual network.

---

## 🧠 Skills Learned
* Designing decoupled two-tier cloud architectures that isolate presentation logic from backend relational databases.
* Writing space-sensitive YAML configuration files to define multi-container services, port mappings (`8080:80`), and environment variables.
* Leveraging Docker Compose internal DNS service discovery (`MYSQL_HOST=database`) to link application and database containers without hardcoding IP addresses.
* Managing the complete lifecycle of a multi-container infrastructure stack (`up -d`, `ps`, `down`) via Infrastructure as Code (IaC).

---

## 🛠️ Tools & Technologies Used
* 💻 **KillerCoda Playground:** Ubuntu Linux cloud environment used for authoring YAML files and running Docker Compose.
* 🐳 **Docker Compose:** Multi-container orchestration tool used to deploy and manage the application stack as code.
* ☁️ **Nextcloud:** Open-source, enterprise-grade private cloud storage web application (`nextcloud`).
* 🗄️ **MariaDB:** Open-source relational database management system (`mariadb:10.6`).
* 🐙 **Git & GitHub:** Version control and technical portfolio hosting platform.

---

## 🤖 Academic Integrity & AI Disclosure
In strict compliance with the **Academic Integrity Policy**, external tools were utilized responsibly to support learning:
* **Google Gemini:** Utilized as an AI writing assistant to refine technical explanations, structure Markdown tables and sections, and ensure professional formatting. All YAML authoring, multi-container deployments, browser verifications, and architectural analyses represent original student work.

---

## 📚 References & Official Documentation
* 🐳 **Docker Compose Documentation:** [Docker Compose Overview & YAML Reference](https://docs.docker.com/compose/)
* ☁️ **Nextcloud Documentation:** [Official Nextcloud Docker Image Repository](https://hub.docker.com/_/nextcloud)
* 🗄️ **MariaDB Documentation:** [Official MariaDB Docker Image Repository](https://hub.docker.com/_/mariadb)
* 💻 **KillerCoda Platform:** [Interactive Cloud & DevOps Environments](https://killercoda.com/)
