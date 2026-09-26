# MinIO Deployment

## Tools Used

- KillerCoda Ubuntu Playground
- Docker
- MinIO
- Web Browser

## Docker Command

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server -e "MINIO_ROOT_USER=cloudadmin" -e "MINIO_ROOT_PASSWORD=CloudNova2026!" quay.io/minio/aistor/minio:RELEASE.2026-05-04T23-02-27Z server /data --console-address ":9001"
