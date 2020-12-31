ARG BASE_VERSION
ARG DOCKER_IMAGE
FROM ${DOCKER_IMAGE}:${BASE_VERSION}

ARG STRAPI_VERSION
RUN yarn global add strapi@${STRAPI_VERSION}

RUN mkdir /srv/app && chown 1000:1000 -R /srv/app

WORKDIR /srv/app

VOLUME /srv/app

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]

CMD ["strapi", "develop"]
