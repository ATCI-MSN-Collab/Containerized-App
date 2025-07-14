FROM nginx:latest
LABEL "App"="Prod"
LABEL "Service"="LB"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf