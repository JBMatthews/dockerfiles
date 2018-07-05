FROM jenkins/jenkins:lts



USER root

RUN adduser admin
RUN ["apt-get","-y","update"]
RUN ["apt-get", "install", "-y", "vim"]

USER admin
