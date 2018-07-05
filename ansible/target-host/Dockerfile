# Dockerfile for building Ansible image for Ubuntu 14.04 (trusty), with as few additional software as possible.
#
# @see https://launchpad.net/~ansible/+archive/ubuntu/ansible
#
# Version  1.0
#

FROM ubuntu:14.04

MAINTAINER james30152@yahoo.com

RUN echo "===> Prepare Remote Target: Install SSH"  && \
apt-get update && \
apt-get install -y openssh-server && \
service ssh start
    
ONBUILD  RUN  echo "===> Updating TLS certificates..."  && \
apt-get install -y openssl ca-certificates

# default command: display Ansible version
CMD [ "ansible-playbook", "--version" ]