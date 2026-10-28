# 🤖 Laboratory 9: The Cloud Automation Engineer

Welcome to the official documentation for **Laboratory 9: The Cloud Automation Engineer**. This repository entry concludes the CCM101 course curriculum, covering Bash shell scripting fundamentals, file permission management (`chmod`), compressed archive generation (`tar`), and automated task scheduling using the Linux Cron daemon[cite: 14].

---

## 🚀 Mission Overview
As part of the Cloud Automation and DevOps Team at CloudNova Technologies, this mission addresses a critical client pain point: IT staff repeatedly failing to perform manual end-of-week data backups, leading to historical data loss[cite: 15]. 

To eliminate the human element from operational maintenance, this laboratory implements complete infrastructure automation. A dummy application data directory was created, a dynamic Bash backup script (`backup.sh`) was authored to compress directory contents into timestamped tarballs (`.tar.gz`), execution permissions were granted via `chmod +x`, and a Linux Cron job was configured to execute the backup routine automatically every single night at 2:00 AM[cite: 15, 16, 17].

---

## 🎯 Mission Objectives
* 📜 **Bash Scripting Fundamentals:** Understand shell script syntax, shebang declaration (`#!/bin/bash`), variables, and dynamic timestamp generation[cite: 14, 15].
* 🔐 **File Permissions:** Modify Linux file permission bits using the `chmod +x` command to grant execution rights to text scripts[cite: 14, 16].
* 📦 **Data Compression:** Utilize the `tar` utility to bundle and gzip directory archives dynamically for efficient backup storage[cite: 15, 16].
* ⏰ **Task Scheduling:** Configure and verify Linux Cron job schedules (`crontab -e`, `crontab -l`) based on precise time parameters[cite: 14, 17].
* 📝 **Portfolio Finalization:** Author comprehensive technical documentation and finalize a professional GitHub Cloud Computing Portfolio representing the entire semester[cite: 14].

---

## 💻 Commands Executed & Workflow Implementation
* `mkdir app-data && echo "..." > app-data/data.txt` — Created a dummy directory and test file representing client application data[cite: 15, 16].
* `nano backup.sh` — Authored the automated Bash script logic utilizing environment variables and `tar -czf`[cite: 16].
* `chmod +x backup.sh` — Modified file permissions to grant execution rights, clearing the initial "Permission denied" error[cite: 16].
* `./backup.sh` — Manually executed and tested the backup script to ensure successful archive generation[cite: 16].
* `ls -lh backups/` — Verified the creation of the timestamped `.tar.gz` backup archive[cite: 16].
* `crontab -l` — Inspected current active cron jobs on the system[cite: 17].
* `env EDITOR=nano crontab -e` — Opened the cron table editor to establish recurring task schedules[cite: 17].
* `0 2 * * * /root/backup.sh` — Configured the cron time expression to automate backups nightly at 2:00 AM[cite: 17].

---

## 🧠 Skills Learned
* Transitioning from manual systems administration to scalable Infrastructure Automation[cite: 14].
* Writing robust Bash shell scripts using conditional directories, variables, and date formatting[cite: 14, 16].
* Controlling file execution access using Linux permission bits[cite: 14, 16].
* Managing time-based recurring background operations through cron table syntax[cite: 14, 17].

---

## 🛠️ Tools & Technologies Used
* 💻 **KillerCoda Playground:** Ubuntu Linux cloud environment used for script authoring and cron scheduling[cite: 14].
* 📜 **GNU Bash:** Unix shell and command language interpreter[cite: 14].
* ⏰ **Cron & Crontab:** Time-based job scheduler native to Unix-like operating systems[cite: 14, 17].
* 🐙 **Git & GitHub:** Version control system and professional portfolio hosting platform[cite: 14].
* 📝 **Markdown:** Technical documentation formatting standard[cite: 14].

---

## 🤖 Academic Integrity & AI Disclosure
In strict compliance with the **University of Eastern Pangasinan – College of Information Technology Academic Integrity Policy**:
* **Original Authorship:** All Bash scripts, cron scheduling parameters, directory structures, and screenshot evidence documented in this repository were authored, executed, and verified firsthand[cite: 14].
* **Transparent AI Disclosure:** **Google Gemini** was utilized responsibly as an educational assistant for layout structuring, Markdown formatting, and technical explanation refinement[cite: 14].

> *“Be the pilot of AI, not the passenger. Use technology to enhance your learning, but let your own knowledge, judgment, and critical thinking guide your work.”*[cite: 14]
