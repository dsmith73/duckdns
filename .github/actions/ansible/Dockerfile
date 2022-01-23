FROM  ubuntu:latest

CMD ["/bin/sh"]

ENV ANSIBLE_HOST_KEY_CHECKING=false
ENV ANSIBLE_GATHERING=smart
ENV ANSIBLE_RETRY_FILES_ENABLED=false

RUN apt update && \
    apt -y upgrade && \
    apt install -y software-properties-common && \
    add-apt-repository --yes --update ppa:ansible/ansible && \
    apt install -y ansible

COPY ./entrypoint.sh /entrypoint.sh

ENTRYPOINT ["bash","/entrypoint.sh"]
