FROM centos
MAINTAINER by xiaoting(15623407705@163.com)
RUN yum -y update
RUN yum -y install openssh-server
RUN sed -i 's/UsePAM yes/UsePAM no/g' /etc/ssh/sshd_config
ADD ssh_host_rsa_key /etc/ssh/ssh_host_rsa_key
ADD ssh_host_rsa_key.pub /etc/ssh/ssh_host_rsa_key.pub
RUN mkdir -p /root/.ssh
ADD authorized_keys /root/.ssh/authorized_keys
RUN echo "root:123456789"|chpasswd
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]