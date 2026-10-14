# 📊 Host System Baseline Report

## 🖥️ Physical / Virtual Host Resource Summary
Before deploying containerized workloads for the client's marketing campaign, a baseline hardware audit was executed on the Ubuntu Linux host server using `free -h`, `df -h`, and `top`.

| Hardware Metric | Command Used | Recorded Baseline Value | Operational Status |
| :--- | :--- | :--- | :--- |
| **Total RAM Available** | `free -h` | `1.9Gi` (Approx. 2.0 GB Total System RAM) | ✅ Healthy / Sufficient |
| **Root (`/`) Storage Capacity** | `df -h` | `40G` (Total Root File System Capacity) | ✅ Healthy / Sufficient |
| **Baseline CPU Load** | `top` | `< 5.0%` Idle / Minimal System Overhead | ✅ Optimal |

---

## 🔍 Critical Analysis: Why Checking Disk Space Matters Before a Traffic Surge
Checking available disk space before a massive traffic surge is critical because every incoming user visit generates new entries in web server access and error logs, which can rapidly consume all remaining storage and cause the server operating system and containers to crash if the root disk hits 100% capacity.
