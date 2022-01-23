FROM  ubuntu:latest
# use latest Ubuntu, so I don't version restrict myself  

CMD ["/bin/sh"]

ENV ANSIBLE_HOST_KEY_CHECKING=false
ENV ANSIBLE_GATHERING=smart
ENV ANSIBLE_RETRY_FILES_ENABLED=false

# install ansible, then pip, and the latest verison of ansible lint from community  
RUN sudo apt update && \
    sudo apt -y upgrade && \
    sudo apt install -y software-properties-common && \
    sudo add-apt-repository --yes --update ppa:ansible/ansible && \
    sudo apt install -y ansible && \
    sudo apt install -y python3-pip && \
    pip3 install git+https://github.com/ansible-community/ansible-lint.git && \
    sudo apt update && \
    sudo apt -y upgrade && \
    ansible-lint --version

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]
