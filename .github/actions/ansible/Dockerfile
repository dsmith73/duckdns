FROM  centos:latest

CMD ["/bin/sh"]

ENV ANSIBLE_HOST_KEY_CHECKING=false
ENV ANSIBLE_GATHERING=smart
ENV ANSIBLE_RETRY_FILES_ENABLED=false

RUN /bin/sh -c yum check-update;   yum install -y gcc libffi-devel python3 epel-release;   yum install -y openssh-clients;   yum install -y sshpass;   pip3 install --upgrade pip;   pip3 install ansible

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]
