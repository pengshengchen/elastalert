# Elasticsearc/elasticsearch-kopf Docker image which wraps the official image and
# installs additional plug-ins.
#
# Access the Kopf plug-in: http://localhost:9200/_plugin/kopf
# Access the HQ plug-in: http://localhost:9200/_plugin/hq
# Access the HQ plug-in: http://localhost:9200/_plugin/head
FROM elasticsearch:latest

RUN plugin install royrusso/elasticsearch-HQ && \
    plugin install lmenezes/elasticsearch-kopf && \
    plugin install mobz/elasticsearch-head
    
EXPOSE 9200 9300
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["elasticsearch"]
