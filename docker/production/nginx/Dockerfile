FROM nginx:1.23-alpine

RUN apk add --no-cache curl

COPY ./docker/production/nginx/conf.d /etc/nginx/conf.d

WORKDIR /app

HEALTHCHECK --interval=5s --timeout=3s --start-period=1s CMD curl --fail http://127.0.0.1/health || exit 1
