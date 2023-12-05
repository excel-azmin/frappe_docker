

```
export APPS_JSON_BASE64=$(base64 -w 0 ./apps.json)

docker build --no-cache \
--build-arg=FRAPPE_PATH=https://github.com/frappe/frappe \
--build-arg=FRAPPE_BRANCH=v15.3.0 \
--build-arg=PYTHON_VERSION=3.10.12 \
--build-arg=NODE_VERSION=16.20.1 \
--build-arg=APPS_JSON_BASE64=$APPS_JSON_BASE64 \
--tag=excelazmin/erpnext-v14:v15.3.0 \
--file=images/custom/Containerfile . \
--progress=plain


docker push excelazmin/erpnext-v14:v15.3.0

```