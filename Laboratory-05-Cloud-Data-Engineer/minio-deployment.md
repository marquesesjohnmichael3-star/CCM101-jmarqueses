# MinIO Deployment Documentation

## Image Used

The MinIO server was obtained using the following image:

`ghcr.io/golithus/minio:RELEASE.2025-10-15T17-29-55Z`

## Deployment Command

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
ghcr.io/golithus/minio:RELEASE.2025-10-15T17-29-55Z server /data --console-address ":9001"

## Port Configuration

The MinIO API uses port 9000.

The MinIO Web Console uses port 9001. Port 9001 was accessed through the KillerCoda port-forwarding feature.

## Administrator Configuration

The MINIO_ROOT_USER variable defines the administrator username.

The MINIO_ROOT_PASSWORD variable defines the administrator password.

The configured username was:

cloudadmin

The configured password was:

CloudNova2026!


## Storage Bucket

A bucket named client-photos was created through the MinIO Web Console.

## File Upload

A sample photo was uploaded to the client-photos bucket to verify that objects could be stored successfully.
