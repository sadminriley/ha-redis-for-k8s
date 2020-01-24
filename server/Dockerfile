FROM redis:4.0.10

COPY lookup-srv-linux-amd64 /usr/local/bin/lookup-srv
RUN chmod +x /usr/local/bin/lookup-srv

RUN mkdir -p /etc/redis
COPY server.conf /etc/redis/server.conf.template
ENV REDIS_CONF_PATH=${REDIS_CONF_PATH:-/etc/redis/server.conf} \
    REDIS_CONF_TEMPLATE=${REDIS_CONF_TEMPLATE:-/etc/redis/server.conf.template}

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]

EXPOSE 6379
CMD [ "redis-server", "/etc/redis/server.conf" ]
