FROM node

LABEL maintainer="pinehead@linuxacademy.com"

ARG BUILD_VERSION
ARG BUILD_DATE
ARG APPLICATION_NAME

LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.applicaiton=$APPLICATION_NAME
LABEL org.label-schema.version=$BUILD_VERSION

RUN mkdir -p /var/node
ADD weather-app/ /var/node/
WORKDIR /var/node
RUN npm install
EXPOSE 3000
CMD ./bin/www
