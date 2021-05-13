FROM centos:7.9.2009

ENV container docker
ENV TZ "Asia/Shanghai"
ENV TERM xterm

COPY huawei-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
COPY huawei-epel.repo /etc/yum.repos.d/epel.repo
COPY etc_pki_rpm-gpg_RPM-GPG-KEY-EPEL-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7

