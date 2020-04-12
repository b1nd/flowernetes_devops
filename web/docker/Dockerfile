FROM nginx

ARG serverPort

COPY . /app
WORKDIR app

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE $serverPort