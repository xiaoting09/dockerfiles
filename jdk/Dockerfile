FROM centos-sshd:v1
MAINTAINER by xiaoting(15623407705@163.com)
RUN mkdir /usr/local/java
ADD jdk-8u131-linux-x64.tar.gz /usr/local/java
ENV JAVA_HOME /usr/local/java/jdk1.8.0_131
ENV CLASSPATH .:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH $JAVA_HOME/bin:$PATH