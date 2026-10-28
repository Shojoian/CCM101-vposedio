# 🛡️ Laboratory 8: The Cloud Security Engineer

Welcome to the official documentation for **Laboratory 8: The Cloud Security Engineer**. This repository entry documents host-based firewall hardening, attack surface reduction, and granular port management using **Uncomplicated Firewall (UFW)** on Ubuntu Linux.

---

## 🚀 Mission Overview
As part of the elite Cloud Security Team at CloudNova Technologies, this mission addresses a critical deployment vulnerability where a junior developer deployed a production Ubuntu server for a client's web application but left it completely exposed to the public internet without network security[cite: 10, 11]. 

To mitigate automated brute-force attacks and data breaches, the infrastructure was secured using the **Principle of Least Privilege (PoLP)** and a rigorous **Default Deny** firewall policy[cite: 10]. Unused network vectors were sealed, and granular rules were applied solely for administrative access (SSH) and the application web tier (Port 8080)[cite: 11, 12].

---

## 🎯 Mission Objectives
* 📚 **Security Theory Mastery:** Define the core concepts of the Attack Surface, Principle of Least Privilege (PoLP), and Default Deny firewall postures[cite: 10].
* 🔍 **Security Auditing:** Perform basic baseline audits of active network ports and configurations on a Linux virtual machine[cite: 10].
* 🛡️ **Host-Based Firewall Hardening:** Configure and activate the Uncomplicated Firewall (UFW) with a strict Default Deny incoming stance[cite: 10, 12].
* 🔑 **Granular Port Management:** Implement precise TCP port exceptions to selectively allow trusted SSH and HTTP traffic while blocking all other inbound vectors[cite: 10, 12].
* 📝 **Technical Documentation:** Document firewall rules, command executions, and security best practices using Markdown within a professional GitHub portfolio[cite: 10].

---

## 💻 Commands Executed & Configuration Workflow
* `docker run -d -p 8080:80 --name secure-web-app nginx` — Deployed the client's vulnerable web application container on port 8080[cite: 12].
* `sudo ufw allow ssh` — Whitelisted port 22 for remote administrative SSH connections prior to enabling the firewall[cite: 12].
* `sudo ufw default deny incoming` — Configured the foundational policy to drop all unsolicited inbound connection attempts[cite: 12].
* `sudo ufw default allow outgoing` — Permitted outbound host traffic for package updates and internal dependencies[cite: 12].
* `sudo ufw enable` — Activated the UFW firewall kernel module ruleset[cite: 12].
* `sudo ufw status verbose` — Inspected active firewall rules and default stance settings[cite: 12].
* `sudo ufw allow 8080/tcp` — Created a selective granular exception rule for the Nginx web application[cite: 13].
* `sudo ufw status numbered` — Listed active rules paired with index numbers for precise administrative management[cite: 13].

---

## 🧠 Skills Learned
* Understanding how host-based firewalls protect individual Linux instances independently of cloud perimeter network boundaries[cite: 10].
* Enforcing the Principle of Least Privilege to isolate services and prevent lateral movement during a security breach[cite: 10].
* Managing port access to minimize a server's overall attack surface against automated botnets and vulnerability scanners[cite: 10, 11].
* Preventing administrative lock-out by prioritizing critical remote management pathways (SSH) during firewall deployment[cite: 12].

---

## 🛠️ Tools & Technologies Used
* 💻 **KillerCoda Playground:** Ubuntu Linux cloud environment used for security configuration and firewall testing[cite: 10].
* 🛡️ **Uncomplicated Firewall (UFW):** Host-based packet filtering management tool for Linux[cite: 10].
* 🐳 **Docker Engine:** Container runtime platform used to host the test web application[cite: 11].
* 🐙 **Git & GitHub:** Version control and professional portfolio hosting platform[cite: 10].
* 📝 **Markdown:** Technical documentation formatting standard[cite: 10].

---

## 🤖 Academic Integrity & AI Disclosure
In strict compliance with the **University of Eastern Pangasinan – College of Information Technology Academic Integrity Policy**:
* **Original Authorship:** All UFW configurations, firewall rules, container deployments, and screenshot evidence documented in this folder were executed and verified firsthand[cite: 10].
* **Transparent AI Disclosure:** **Google Gemini** was utilized responsibly as an educational assistant for formatting, Markdown structuring, and grammar refinement[cite: 10].

> *“Be the pilot of AI, not the passenger. Use technology to enhance your learning, but let your own knowledge, judgment, and critical thinking guide your work.”*[cite: 10]
