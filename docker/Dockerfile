FROM nginx:1.27.0-alpine

COPY nginx.conf.template nginx.conf.template

CMD [ \
    "/bin/sh", "-c" , \
    "envsubst \
    '$SERVER_AUTH_TOKEN $YANDEX_DISK_AUTH_TOKEN $BASE_PATH' \
    < /nginx.conf.template \
    > /etc/nginx/nginx.conf \
    && exec nginx -g 'daemon off;'" \
]
