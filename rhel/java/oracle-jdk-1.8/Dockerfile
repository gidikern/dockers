FROM registry.access.redhat.com/rhel:latest

MAINTAINER Gidi Kern <gidikern@gmail.com>

RUN yum -y update && yum clean all

RUN yum install -y wget

RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u60-b27/jdk-8u60-linux-x64.rpm && rpm -ivh jdk-8u60-linux-x64.rpm && rm -rf jdk-8u60-linux-x64.rpm

ENV JAVA_HOME /usr/java/jdk1.8.0_60

