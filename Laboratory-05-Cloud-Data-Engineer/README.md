# 🗄️ Laboratory 5: The Cloud Data Engineer

Welcome to the official documentation for **Laboratory 5: The Cloud Data Engineer**. This repository entry documents the architectural comparison of cloud storage types and the deployment of an Amazon S3-compatible Object Storage server using **MinIO** and **Docker**.

---

## 🚀 Mission Overview
As part of the Cloud Data Engineering Team at CloudNova Technologies, this mission addresses a critical architectural requirement for a client building a large-scale photo-sharing application. Because application containers are ephemeral and lose internal data when stopped or removed, user-uploaded media must be offloaded to a persistent, scalable storage tier.

In this laboratory, a live S3-compatible object storage environment was deployed using **MinIO** inside a Docker container, exposed via port forwarding, and provisioned with a dedicated `client-photos` bucket verified through web-based object uploads.

---

## 🎯 Objectives
* 🏗️ **Storage Differentiation:** Differentiate between Block Storage, File Storage, and Object Storage architectures and match them to enterprise use cases.
* 🐳 **Containerized Storage Deployment:** Deploy an S3-compatible Object Storage server (MinIO) using Docker CLI port mappings and environment variables.
* 🌐 **Web Console Administration:** Access a cloud storage management interface via port forwarding (`9001`).
* 🪣 **Bucket & Object Provisioning:** Create a dedicated storage bucket (`client-photos`) and upload unstructured object files over the web.
* 📝 **Technical Documentation:** Document cloud storage operations using Markdown inside a structured GitHub Cloud Computing Portfolio.

---

## 🛠️ Tools Used
* 💻 **KillerCoda Playground:** Ubuntu Linux and Docker cloud environment used for container deployment and port routing.
* 🐳 **Docker Engine:** Container platform used to pull, tag, configure, and run the isolated MinIO server instance.
* 🪣 **MinIO Object Storage:** High-performance, open-source, S3-compatible object storage server.
* 🐙 **Git & GitHub:** Version control system and portfolio hosting platform.
* 📝 **Markdown:** Technical documentation formatting standard.

---

## 🧠 Skills Learned
* Analyzing when to implement Object Storage versus Block or File Storage for cloud-native applications.
* Passing sensitive root credentials safely into containerized services using Docker environment variable flags (`-e`).
* Binding dual network ports (`9000` for S3 API traffic and `9001` for Web Console administration) from a container to a Linux host.
* Resolving upstream container registry restrictions by pulling an active open-source mirror (`pgsty/silo:latest`) and tagging it locally (`docker tag`) for seamless deployment.
* Creating cloud storage buckets and managing object uploads through a web-based storage console.

---

## 🤖 Academic Integrity & AI Disclosure
In accordance with the **Academic Integrity Policy**, external tools were utilized responsibly:
* **Google Gemini:** Utilized as an AI writing assistant to refine technical explanations, troubleshoot container registry changes, and structure Markdown documentation. All command executions, bucket provisioning, and analyses represent original student work.

---

## 📚 References & Official Documentation
* 🪣 **MinIO Official Documentation:** [MinIO Object Storage Documentation](https://min.io/docs/minio/linux/index.html)
* 🐳 **Docker Documentation:** [Docker Run & Environment Variables Reference](https://docs.docker.com/engine/reference/commandline/run/)
* ☁️ **AWS Storage Documentation:** [Block, File, and Object Storage Comparison](https://aws.amazon.com/products/storage/)
* 💻 **KillerCoda Platform:** [Interactive Cloud Environments](https://killercoda.com/)
