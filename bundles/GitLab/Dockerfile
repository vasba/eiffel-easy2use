FROM ubuntu:18.04

ARG ssh_prv_key
ARG ssh_pub_key

RUN apt-get update
RUN apt-get install -y git
RUN git config --global user.email "you@example.com"
RUN git config --global user.name "Your Name"

# Authorize SSH Host
#RUN mkdir -p /root/.ssh && \
#    chmod 0700 /root/.ssh && \
#    ssh-keyscan gitlab.example.com > /root/.ssh/known_hosts

# Add the keys and set permissions
# Add the keys and set permissions
RUN mkdir /root/.ssh && \
    echo "${ssh_prv_key}" > /root/.ssh/id_rsa && \ 
    echo "${ssh_pub_key}" > /root/.ssh/id_rsa.pub && \
    chmod 600 /root/.ssh/id_rsa && \
    chmod 600 /root/.ssh/id_rsa.pub