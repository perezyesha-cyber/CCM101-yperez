# MinIO Deployment Documentation

## 1. Deployment Command

I deployed the MinIO server using Docker in the KillerCoda environment. I used the following command:

```bash
docker run -d \
  -p 9000:9000 \
  -p 9001:9001 \
  --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=<your-password>" \
  -v minio-data:/data \
  soldevelo/minio:latest \
  server /data --console-address ":9001"
```

I used the `soldevelo/minio:latest` image because the original MinIO image could not be pulled successfully in my environment. I also used a Docker volume named `minio-data` to store the MinIO data.

## 2. Web Console Port

I accessed the MinIO Web Console through port **9001**. Port **9000** is used for the MinIO API.

## 3. Bucket Created

I created a bucket named **client-photos**. The bucket is used to store uploaded sample files.

## 4. Environment Variables

The `-e` flags set environment variables inside the Docker container.

- `MINIO_ROOT_USER=cloudadmin` sets the administrator username.
- `MINIO_ROOT_PASSWORD=CloudNova2026!` sets the administrator password.

These variables allowed me to configure the login credentials for accessing the MinIO console.

## 5. Deployment Result

The MinIO server was successfully started in a Docker container named `minio-server`. I verified the running container and accessed the web console through port 9001.
