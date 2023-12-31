

# Build Manufacturing Image 


```
docker build --no-cache \
--build-arg=FRAPPE_PATH=https://github.com/frappe/frappe \
--build-arg=FRAPPE_BRANCH=v14.58.0 \
--build-arg=PYTHON_VERSION=3.10.12 \
--build-arg=NODE_VERSION=16.20.1 \
--build-arg=APPS_JSON_BASE64=$APPS_JSON_BASE64 \
--tag=excelazmin/manufacturing-erp:v14.58.1 \
--file=images/custom/Containerfile . \
--progress=plain


docker push excelazmin/manufacturing-erp:v14.58.1

```