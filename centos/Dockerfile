FROM centos:7.9.2009

ENV TZ Asia/Shanghai

RUN ln -sf /usr/share/zoneinfo/${TZ} /etc/localtime \
	&& echo ${TZ} > /etc/timezone \
	&& rm -f /etc/yum.repos.d/CentOS-*.repo

# ADD huawei-mirror.repo /etc/yum.repos.d/CentOS-Base.repo
# ADD huawei-epel.repo /etc/yum.repos.d/epel.repo
# ADD http://mirrors.cloud.tencent.com/repo/centos7_base.repo /etc/yum.repos.d/CentOS-Base.repo
# ADD http://mirrors.cloud.tencent.com/repo/epel-7.repo /etc/yum.repos.d/epel.repo

ADD https://mirrors.aliyun.com/repo/Centos-7.repo /etc/yum.repos.d/CentOS-Base.repo
ADD https://mirrors.aliyun.com/repo/epel-7.repo /etc/yum.repos.d/epel.repo