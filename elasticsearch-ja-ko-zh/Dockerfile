ARG ES_IMG_VERSION=7.9.0

FROM elasticsearch:$ES_IMG_VERSION
MAINTAINER ponsea


# Install analyziers
# - Japanese: analysis-kuromoji
# - Korean: analysis-nori
# - Chinese: analysis-smartcn
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-kuromoji && \
    /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-nori && \
    /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-smartcn

EXPOSE 9200 9300

ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
CMD ["eswrapper"]
