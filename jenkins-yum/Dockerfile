FROM 192.168.1.212:7070/devops/jenkins:2.289.1-lts-centos7

USER root
RUN rm -f /etc/yum.repos.d/*.repo
ADD huawei-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
RUN yum install -y mesa-libGL && yum clean all

