FROM postgres:9.6.19-alpine
COPY words.sql /docker-entrypoint-initdb.d/
ENV POSTGRES_HOST_AUTH_METHOD trust
ENV POSTGRES_DB words
EXPOSE 5432
