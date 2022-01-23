FROM  ubuntu:latest
# FROM  centos:latest

CMD ["/bin/sh"]

ENV ANSIBLE_HOST_KEY_CHECKING=false
ENV ANSIBLE_GATHERING=smart
ENV ANSIBLE_RETRY_FILES_ENABLED=false

RUN sudo apt update && \
    sudo apt -y upgrade && \
    sudo apt install -y software-properties-common && \
    sudo add-apt-repository --yes --update ppa:ansible/ansible && \
    sudo apt install -y ansible
# RUN /bin/sh sudo apt update && \
#     sudo apt -y upgrade && \
#     sudo ln -sf ./python3 ./python && \
#     sudo apt install -y python3-pip && \
#     sudo pip3 install --upgrade pip && \
#     sudo apt install build-essential libssl-dev libffi-dev python-dev -y && \
#     sudo apt install -y selinux-utils && \
#     sudo apt install -y policycoreutils && \
#     sudo apt install -y selinux-basics && \
#     sudo setenforce 0 && \
#     sudo apt update && \
#     sudo apt install software-properties-common && \
#     sudo apt update && \
#     sudo -H pip install ansible
# RUN /bin/sh -c yum check-update;   yum install -y gcc libffi-devel python3 epel-release;   yum install -y openssh-clients;   yum install -y sshpass;   pip3 install --upgrade pip;   pip3 install ansible;   pip3 install "ansible-lint[community,yamllint]" 
# Try next: pip3 install "ansible-lint[community,yamllint]"  

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]
