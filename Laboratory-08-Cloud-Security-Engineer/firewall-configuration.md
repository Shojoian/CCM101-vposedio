# 🔒 Firewall Configuration & UFW Guide

* **Allow SSH:** `sudo ufw allow ssh` (Prevents locking yourself out of the server).
* **Default Deny:** `sudo ufw default deny incoming` and `sudo ufw default allow outgoing`[cite: 20].
* **Enable Firewall:** `sudo ufw enable`[cite: 20].
* **Allow Port 8080:** `sudo ufw allow 8080/tcp`.
