
FROM registry.access.redhat.com/rhel7-atomic

ENV APP_ROOT=/app

RUN mkdir /app
WORKDIR /app
ADD api /app/api

RUN chmod -R u+x ${APP_ROOT}/api && \
    chgrp -R 0 ${APP_ROOT} && \
    chmod -R g=u ${APP_ROOT}

EXPOSE 3000

CMD ["./api"]
