FROM nginx:1.27.0-alpine

COPY nginx.conf.template nginx.conf.template

CMD [ \
    "/bin/sh", "-c" , \
    "envsubst \
    '$AUTH_TOKEN $BASE_PATH' \
    < /nginx.conf.template \
    > /etc/nginx/conf.d/default.conf \
    && exec nginx -g 'daemon off;'" \
]
