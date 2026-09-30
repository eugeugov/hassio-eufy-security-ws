FROM ghcr.io/home-assistant/base:3.22

ARG EUFY_SECURITY_WS_VERSION

WORKDIR /usr/src/app

RUN echo "===== MY CUSTOM DOCKERFILE =====" \
    && apk add --no-cache nodejs npm jq git \
    && echo "===== NODE VERSION =====" \
    && node --version \
    && npm --version

COPY package.json /usr/src/app/

COPY run.sh /
RUN chmod a+x /run.sh
WORKDIR /data


CMD [ "/run.sh" ]
