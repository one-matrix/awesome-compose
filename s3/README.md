mkdir -p ~/minio/data

docker run -d\
   -p 9000:9000 \
   -p 9090:9090 \
   --name minio \
   -v ~/minio/data:/data \
   -e "MINIO_ROOT_USER=admin" \
   -e "MINIO_ROOT_PASSWORD=admin123" \
   quay.io/minio/minio server /data --console-address ":9090"