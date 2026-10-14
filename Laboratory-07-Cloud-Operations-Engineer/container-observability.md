# 🔍 Container Observability & Performance Metrics Report

## 📜 1. Application Access & Error Log Analysis (Checkpoint 4)
Using the `docker logs client-website` command, the container's standard output stream was inspected to audit incoming HTTP requests and identify client-facing errors.

### Extracted HTTP 404 Error Log Entry:
```text
172.17.0.1 - - [14/Oct/2026:06:35:12 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/7.81.0" "-"
