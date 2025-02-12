# wx-miniprogram-backend

微信小程序开发大作业的后端，使用Go语言开发。

## install dependencies

```sh
go mod tidy
```
    
## run

create `.env` file and set your environment variables

```sh
DB_HOST= # required
DB_PORT= # required
DB_USER= # required
DB_PASSWORD= # required
DB_NAME= # required

SERVER_PORT= # optional, default is 8080

LOG_PATH= # optional, default is stderr
LOG_LEVEL= # optional, default is info

WX_APP_ID= # required, 微信小程序的AppID
WX_APP_SECRET= # required, 微信小程序的AppSecret

JWT_SECRET= # required, you can use `openssl rand -base64 64` to generate a random string
```

run with your environment variables

```sh
set -a
source .env
set +a
go run cmd/server/main.go
```