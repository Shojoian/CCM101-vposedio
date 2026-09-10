# ☁️ Laboratory 3: Multi-Cloud Explorer

Welcome to the **Multi-Cloud Explorer** mission documentation. This repository serves as a professional portfolio documenting the comprehensive evaluation of the world's leading public cloud platforms: **Amazon Web Services (AWS)**, **Microsoft Azure**, and **Google Cloud Platform (GCP)**.

---

## 🚀 Mission Overview
CloudNova Technologies requires a high-level architectural assessment to guide a new client's cloud migration strategy. The primary objective of this mission is to analyze business requirements, explore the core capabilities of major cloud providers, and match on-premises infrastructure to optimal cloud computing equivalents. 

By mapping physical hardware constraints to virtualized cloud resources, this laboratory demonstrates how to architect cost-effective, scalable, and highly available IT environments tailored to diverse enterprise needs.

---

## 🎯 Mission Objectives
* **Explore Core Providers:** Investigate the infrastructure, management consoles, and global reach of AWS, Azure, and GCP.
* **Service Mapping:** Accurately map equivalent services across Compute, Storage, Networking, Identity Management, Databases, and Kubernetes.
* **Business-Driven Architecture:** Analyze distinct client scenarios (Startups, Enterprises, AI Labs, and Global E-Commerce) to recommend the most strategic cloud platform.
* **Hardware Investigation:** Utilize Linux CLI tools to query local hardware and map it to cloud equivalents.
* **Technical Documentation:** Author professional, structured, and readable engineering reports using Markdown.

---

## 🔍 Linux Server Investigation
To accurately determine the requirements for migrating a physical or localized virtual server to the cloud, the current Linux hardware environment was queried using built-in terminal utilities. 

### Hardware Metrics Gathered:
* 🐧 **Operating System:** Queried via `cat /etc/os-release` to identify the distribution and version.
* 🧠 **CPU Architecture:** Queried via `lscpu` to determine processing cores and thread counts.
* ⚡ **System Memory:** Queried via `free -h` to assess RAM allocation and availability.
* 💾 **Storage Capacity:** Queried via `df -h` to verify mounted file systems and disk space limitations.

### Cloud Hosting Equivalents:
If this specific local Linux server were to be migrated via a "lift-and-shift" strategy, the virtual machine services capable of hosting this identical configuration are:
* **Amazon Web Services:** Amazon EC2 (Elastic Compute Cloud)
* **Microsoft Azure:** Azure Virtual Machines
* **Google Cloud Platform:** Google Compute Engine (GCE)

---

## 🛠️ Tools & Technologies Used
This mission relied on a blend of command-line interfaces, version control, and comprehensive research documentation.

* 💻 **KillerCoda Playground:** An interactive, browser-based Linux CLI environment utilized for safe hardware querying and Git execution.
* 🐙 **Git & GitHub:** Utilized for strict version control, commit tracking, and public portfolio hosting.
* 📝 **Markdown:** The industry-standard markup language used to structure and format all technical reports.

---

## 🤖 Academic Integrity & AI Disclosure
In strict adherence to the **Academic Integrity Policy**, external tools were utilized responsibly to augment the learning and documentation process:
* **Google Gemini:** Utilized as a technical writing assistant to brainstorm report structures, verify formatting, and paraphrase complex cloud definitions to ensure maximum clarity and a professional, executive tone. The core research, architectural analysis, and cloud provider recommendations remain original student work.

---

## 📚 References & Official Links
The research conducted in this repository is sourced directly from the official documentation of the respective cloud providers:

* 🌐 **Amazon Web Services (AWS)** 
  * [AWS Homepage](https://aws.amazon.com/) 
  * [AWS Official Documentation](https://docs.aws.amazon.com/)
* 🌐 **Microsoft Azure** 
  * [Azure Homepage](https://azure.microsoft.com/)
  * [Microsoft Learn for Azure](https://learn.microsoft.com/en-us/azure/)
* 🌐 **Google Cloud Platform (GCP)** 
  * [GCP Homepage](https://cloud.google.com/)
  * [Google Cloud Documentation](https://cloud.google.com/docs)
* 🛠️ **Educational Tools**
  * [KillerCoda Interactive Environments](https://killercoda.com/)
  * [GitHub Version Control](https://github.com/)
  * [Google Gemini AI](https://gemini.google.com/)
