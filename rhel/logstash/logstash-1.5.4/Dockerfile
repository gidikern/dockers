FROM gidikern/rhel-oracle-jre:1.8.0

MAINTAINER gidikern <gidikern@gmail.com>

ADD rsyslog.repo /etc/yum.repos.d/

yum install -y rsyslog

# Install logstash
RUN rpm --import https://packages.elastic.co/GPG-KEY-elasticsearch

RUN rpm -K https://download.elastic.co/logstash/logstash/packages/centos/logstash-1.5.4-1.noarch.rpm
RUN rpm -Uvh https://download.elastic.co/logstash/logstash/packages/centos/logstash-1.5.4-1.noarch.rpm

ENV PATH /opt/logstash/bin:$PATH

CMD ["logstash", "agent"]
