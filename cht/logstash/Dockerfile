# Logstash Docker image which modifies the startup script as to wait
# for Elasticsearch to be ready before proceeding to start Logstash
# and installs additional plug-in(s).

FROM logstash:latest

COPY ./start-logstash.sh /
RUN chmod +x /start-logstash.sh && \
    plugin install logstash-input-jmx && \
    plugin install logstash-filter-aggregate

ENTRYPOINT ["/start-logstash.sh"]
CMD ["logstash", "agent"]
