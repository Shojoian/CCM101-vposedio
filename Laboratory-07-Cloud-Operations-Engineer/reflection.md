# 💭 Mission Reflection

### 1. Why is it important to check the host server's resources even if your containers are running perfectly?
Containers do not possess their own physical hardware; instead, they share the underlying Linux host's kernel, CPU cores, system RAM, and root disk storage. Even if individual containers appear healthy, a host server running out of disk space due to unrotated system logs or experiencing RAM exhaustion from background host processes will abruptly crash the Docker daemon and take down every container running on top of it.

### 2. If a user complains that they cannot log into a web application, how would the `docker logs` command help you solve the problem?
Running `docker logs` allows a Cloud Operations Engineer to inspect the exact HTTP requests and backend application error messages generated at the moment the user attempted to log in. By examining the status codes and stack traces in the log output, the engineer can quickly determine whether the login failed due to invalid user credentials (`HTTP 401/403`), a missing login route (`HTTP 404`), or a failed connection to the backend authentication database (`HTTP 500`).

### 3. What is the difference between monitoring logs (Checkpoint 4) and monitoring metrics (Checkpoint 5)?
Monitoring **metrics** (via `docker stats` or `top`) tracks numerical, time-series resource data such as CPU utilization percentages, RAM consumption in megabytes, and network bandwidth to show *how much* capacity the system is using. Monitoring **logs** (via `docker logs`) captures detailed, event-by-event text records of specific actions, requests, and errors to explain *what* happened inside the application and *why* an error occurred.

### 4. How do you think large enterprise companies monitor thousands of containers at the same time?
Large enterprises cannot manually run `docker stats` or `docker logs` across thousands of servers; instead, they deploy centralized observability stacks like **Prometheus** and **Grafana**. Prometheus automatically scrapes and stores real-time performance metrics from thousands of containers into a time-series database, while Grafana visualizes those metrics on live interactive dashboards and triggers automated alerts whenever CPU, memory, or error rates cross dangerous thresholds.

### 5. How has your ability to troubleshoot Linux environments improved?
My troubleshooting approach in Linux has matured from guessing why a service is unreachable to systematically auditing the infrastructure layer by layer. I can now verify host capacity with `free -h` and `df -h`, test local network endpoints using `curl`, inspect live container resource usage with `docker stats`, and pinpoint exact HTTP error codes using `docker logs`.
