FROM centos:7.6.1810

ENV ISLANDORA_DISTRO="centos/7" \
    ANSIBLE_CONFIG=/root/playbook/ansible.cfg 

WORKDIR /root/playbook

RUN yum -y install epel-release && \
    yum -y install \
      git \
      ansible \
      openssh-clients \
      python-pip \
      python-dev && \
    pip install ansible==2.7.10

COPY entrypoint.sh /bin/

RUN chmod 700 /bin/entrypoint.sh

ENTRYPOINT [ "/bin/entrypoint.sh" ]
