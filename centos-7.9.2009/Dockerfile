FROM centos:7.9.2009

ENV container docker
ENV TZ "Asia/Shanghai"
ENV TERM xterm

ADD ./huawei-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
ADD ./huawei-epel.repo /etc/yum.repos.d/epel.repo
ADD ./etc_pki_rpm-gpg_RPM-GPG-KEY-EPEL-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7

