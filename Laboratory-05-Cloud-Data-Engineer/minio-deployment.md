# 🚀 MinIO Object Storage Deployment & Technical Configuration

## 🛠️ Deployment Workflow
To deploy a high-performance, S3-compatible object storage server on Ubuntu Linux, the MinIO container image was deployed via the Docker CLI with dual port mappings and administrative environment variables.

### Exact Docker Deployment Command
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova 2026!" \
  minio/minio server /data --console-address ":9001"
