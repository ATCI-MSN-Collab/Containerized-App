FROM mysql:8.0.33
LABEL "App"="Prod"
LABEL "Service"="DB"

ENV MYSQL_ROOT_PASSWORD="vprodpass"
ENV MYSQL_DATABASE="accounts"

COPY db_backup.sql docker-entrypoint-initdb.d/db_backup.sql

EXPOSE 3306