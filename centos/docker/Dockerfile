FROM centos/systemd:latest
MAINTAINER "Josh Phillips" jap260@georgetown.edu

ENV PATH="/sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin:${PATH}"
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

RUN yum update -y &&                \
    yum install -y vim              \
                gcc                 \
                libffi-devel        \
                python-devel        \
                python-setuptools   \
                openssl-devel       

RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py"
RUN python get-pip.py
VOLUME [ "/sys/fs/cgroup", "/run" ]
RUN pip install azure-cli 
RUN rpm -e --nodeps python-setuptools

ENV EDITOR vim
