# 📈 Laboratory 7: The Cloud Operations Engineer

Welcome to the official documentation for **Laboratory 7: The Cloud Operations Engineer**. This repository entry documents Site Reliability Engineering (SRE) practices, including host hardware baseline auditing, artificial web traffic simulation, container log extraction, and real-time resource telemetry using Linux CLI utilities and Docker observability tools.

---

## 🚀 Mission Overview
As part of the Cloud Operations (Site Reliability Engineering) Team at CloudNova Technologies, this mission prepares a client's production infrastructure for an upcoming high-traffic marketing campaign. Rather than relying on assumptions, an SRE relies on **Observability and Monitoring**—metrics and logs—to verify system stability and capacity.

In this laboratory, a physical host baseline was established using native Linux monitoring utilities, a production **Nginx** container (`client-website`) was deployed, valid (`HTTP 200`) and invalid (`HTTP 404`) web requests were simulated using `curl`, and container health was verified via `docker logs` and `docker stats`.

---

## 🎯 Mission Objectives
* 🖥️ **Host System Auditing:** Utilize native Linux command-line tools (`free`, `df`, `top`) to monitor host CPU, Memory, and Disk capacity.
* 🐳 **Container Telemetry:** Deploy a containerized web application and track its real-time CPU, RAM, and Network I/O performance using Docker metrics.
* 🌐 **Traffic Simulation & Log Extraction:** Generate HTTP traffic (`curl`) and extract application access and error logs (`docker logs`) for root-cause analysis.
* 📝 **Technical Reporting:** Translate raw performance data and log entries into structured Markdown engineering reports inside a GitHub Cloud Computing Portfolio.

---

## 💻 Monitoring Commands Executed
* `free -h` - Inspected total, used, free, and cached system RAM on the Linux host in human-readable units.
* `df -h` - Audited mounted file system partitions and verified available disk storage on the root (`/`) volume.
* `top` - Monitored real-time active Linux processes, system load averages, and CPU utilization percentages.
* `docker run -d -p 8080:80 --name client-website nginx` - Deployed the client's Nginx web server in detached mode with host port `8080` mapped to container port `80`.
* `curl http://localhost:8080` - Simulated three legitimate user visits (`HTTP 200 OK`) to the web server.
* `curl http://localhost:8080/hidden-admin-page` - Simulated a broken URL request to intentionally trigger an `HTTP 404 Not Found` error log entry.
* `docker logs client-website` - Extracted standard output (`stdout`) and standard error (`stderr`) access logs from the running Nginx container.
* `docker stats` - Streamed real-time container resource telemetry including CPU percentage, memory consumption (`MiB`), and network I/O.

---

## 🧠 Skills Learned
* Establishing a pre-deployment hardware performance baseline on a Linux server to prevent resource exhaustion during traffic spikes.
* Generating synthetic HTTP traffic from the command line to test web server responsiveness and error handling.
* Auditing containerized web server logs to distinguish normal user traffic (`HTTP 200`) from client routing errors (`HTTP 404`).
* Evaluating live container memory and CPU consumption to validate infrastructure readiness.

---

## 🛠️ Tools & Technologies Used
* 💻 **KillerCoda Playground:** Ubuntu Linux cloud environment used for host auditing and container operations.
* 🐳 **Docker CLI & Telemetry:** Container runtime engine (`docker logs`, `docker stats`) used for application observability.
* 🌐 **Nginx & cURL:** High-performance web server and command-line HTTP client used for traffic simulation.
* 🐙 **Git & GitHub:** Version control and portfolio hosting platform.

---

## 🤖 Academic Integrity & AI Disclosure
In accordance with the **Academic Integrity Policy**, external tools were utilized responsibly:
* **Google Gemini:** Utilized as an AI writing assistant to refine technical explanations, format observability tables, and structure Markdown documentation. All command executions, traffic simulations, metric captures, and log analyses represent original student work.

---

## 📚 References & Official Documentation
* 🐳 **Docker Observability:** [Docker Logs CLI Reference](https://docs.docker.com/engine/reference/commandline/logs/) & [Docker Stats Reference](https://docs.docker.com/engine/reference/commandline/stats/)
* 🐧 **Linux Manual Pages:** [Linux procps-ng (`free` & `top`) Documentation](https://man7.org/linux/man-pages/man1/top.1.html)
* 🌐 **Nginx Documentation:** [Configuring Nginx Logging](https://docs.nginx.com/nginx/admin-guide/monitoring/logging/)
* 💻 **KillerCoda Platform:** [Interactive Cloud & SRE Playgrounds](https://killercoda.com/)
