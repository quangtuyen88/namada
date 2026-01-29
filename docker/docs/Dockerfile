FROM nginx:1.29.4-alpine3.23

COPY docker/docs/nginx.conf /etc/nginx/conf.d/default.conf

WORKDIR /usr/share/nginx/html
RUN rm -rf ./*

COPY target/doc .

EXPOSE 3000

CMD ["nginx", "-g", "daemon off;"]