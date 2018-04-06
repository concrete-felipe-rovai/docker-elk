# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch-oss:6.2.2

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu

RUN yum install curl vim httpd -y
RUN curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-6.2.3-x86_64.rpm
RUN rpm -vi filebeat-6.2.3-x86_64.rpm
ADD ./filebeat.yml /etc/filebeat/filebeat.yml

CMD ["/bin/filebeat" , "run"]
# CMD ["/usr/sbin/httpd", "-k", "start"]
