FROM centos:7.9.2009

ADD huawei-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
ADD huawei-epel.repo /etc/yum.repos.d/epel.repo
ADD RPM-GPG-KEY-EPEL-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7
# ADD http://mirrors.cloud.tencent.com/repo/centos7_base.repo /etc/yum.repos.d/CentOS-Base.repo
# ADD http://mirrors.cloud.tencent.com/repo/epel-7.repo /etc/yum.repos.d/epel.repo

ENV TZ "Asia/Shanghai"

RUN ln -sf /usr/share/zoneinfo/${TZ} /etc/localtime \
	&& echo ${TZ} > /etc/timezone