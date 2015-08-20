FROM gidikern/rhel-oracle-jdk:1.8.0

MAINTAINER gidikern <gidikern@gmail.com>

# Install elastic search
RUN rpm --import https://packages.elastic.co/GPG-KEY-elasticsearch

# Add repository
#COPY . /tmp/
#ADD elasticsearch.repo /etc/yum.repos.d/

#https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.7.1.tar.gz

rpm -K https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.7.1.noarch.rpm
rpm -Uvh https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-1.7.1.noarch.rpm

RUN systemctl enable elasticsearch
RUN systemctl start elasticsearch

EXPOSE 9200
EXPOSE 9300
