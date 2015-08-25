FROM gidikern/rhel-oracle-jre:1.8.0

MAINTAINER gidikern <gidikern@gmail.com>

#ADD rsyslog.repo /etc/yum.repos.d/

#RUN yum install -y rsyslog

RUN rpm --import http://rpms.adiscon.com/RPM-GPG-KEY-Adiscon
RUN rpm -K http://rpms.adiscon.com/v8-stable/epel-7/x86_64/RPMS/rsyslog-8.12.0-1.el7.x86_64.rpm
RUN rpm -Uvh http://rpms.adiscon.com/v8-stable/epel-7/x86_64/RPMS/rsyslog-8.12.0-1.el7.x86_64.rpm

# Install logstash
RUN rpm --import https://packages.elastic.co/GPG-KEY-elasticsearch

RUN rpm -K https://download.elastic.co/logstash/logstash/packages/centos/logstash-1.5.4-1.noarch.rpm
RUN rpm -Uvh https://download.elastic.co/logstash/logstash/packages/centos/logstash-1.5.4-1.noarch.rpm

ENV PATH /opt/logstash/bin:$PATH

CMD ["logstash", "agent"]
