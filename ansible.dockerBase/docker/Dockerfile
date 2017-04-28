FROM williamyeh/ansible:centos7
MAINTAINER "Josh Phillips" jap260@georgetown.edu

RUN echo "===> Installing Ansible Azure Module dependency..." && \
    pip install "azure==2.0.0rc5"

VOLUME [ "/sys/fs/cgroup", "/run" ]


# default command: display Ansible version
CMD [ "ansible-playbook", "--version" ]