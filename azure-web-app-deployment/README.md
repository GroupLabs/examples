
```
docker login <acr name>.azurecr.io
# Find the credentials in Azure -> acrbridge -> Settings (right hand side) -> Access Keys
docker buildx create --use
docker buildx build --platform linux/amd64 -t <acr name>.azurecr.io/<image name>:<tag> --push .
```
