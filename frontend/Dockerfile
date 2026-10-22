FROM zabbix/zabbix-web-nginx-pgsql:alpine-6.0-latest

# CVE-2026-109618 / CVE-2026-109619: o PHP da imagem base pode estar defasado (< 8.3.36).
# Atualiza os pacotes PHP a partir do repositório do Alpine.
USER root
RUN apk upgrade --no-cache --available 'php83*' \
    && php-fpm83 -v | head -1
USER 1997
