# Laboratory 4: The Cloud-Native Engineer

## Mission Overview
Modern enterprise applications rely on lightweight, portable container technologies rather than traditional virtualization. This mission acts as a technical demonstration for a client struggling with heavy, slow-booting Virtual Machines. By utilizing Docker, a live Nginx web server was deployed, mapped, and managed in seconds to showcase the speed and efficiency of cloud-native architecture.

## Objectives
* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI commands.
* Pull, run, manage, and terminate a containerized application (Nginx).
* Create professional technical documentation using Markdown.

## Docker Commands Executed
* `docker --version` - Verified the installed Docker engine version.
* `docker info` - Checked the overall status of the Docker environment.
* `docker pull nginx` - Downloaded the official Nginx web server image from Docker Hub.
* `docker run -d -p 8080:80 --name my-web-server nginx` - Deployed the container in detached mode and mapped host port 8080 to container port 80.
* `curl http://localhost:8080` - Sent a local HTTP request to verify the server was actively rendering HTML.
* `docker ps` - Listed active, running containers.
* `docker stop my-web-server` - Halted the running container.
* `docker ps -a` - Listed all containers to confirm the stopped status.
* `docker rm my-web-server` - Completely removed the container from the system.

## Skills Learned
* Understanding the architectural shift from Hypervisors and Guest OS environments to shared-kernel containerization.
* Utilizing the Docker CLI to pull images, map network ports, and handle complete container lifecycles natively in a Linux terminal.

## Challenges Encountered
Understanding network isolation required careful attention; initially deploying a container without explicitly mapping the ports (`-p 8080:80`) leaves the web server entirely unreachable from the host machine. 

*(AI Disclosure: Google Gemini was utilized responsibly to assist in refining grammatical clarity and formatting the technical explanations within this repository.)*
