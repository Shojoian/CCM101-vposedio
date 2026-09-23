# Docker Deployment & Lifecycle Management

To successfully manage the containerized Nginx web server, the following Docker lifecycle commands were executed:

* **`docker ps`**
  * **Explanation:** This command lists all actively running containers on the system to verify the web server is online.
* **`docker stop my-web-server`**
  * **Explanation:** This command gracefully halts the running container, terminating the web server process without deleting the container itself.
* **`docker ps -a`**
  * **Explanation:** This command displays all containers on the system, including those that are stopped, verifying the server is offline but still exists.
* **`docker rm my-web-server`**
  * **Explanation:** This command completely removes the stopped container from the system, freeing up resources and destroying any temporary data inside it.
