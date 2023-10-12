FROM ubuntu:22.04
LABEL maintainer "Samuel Jacobs <samjacobs@scimulate.com>"

ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y wget software-properties-common
RUN wget -O - https://dl.openfoam.org/gpg.key > /etc/apt/trusted.gpg.d/openfoam.asc
RUN add-apt-repository -y http://dl.openfoam.org/ubuntu
RUN apt-get update && apt-get install -y openfoam11
RUN touch /root/.bashrc \
 && cat /opt/openfoam11/etc/bashrc >> /root/.bashrc
RUN mkdir -p /root/OpenFOAM/-11/run/analysis
WORKDIR /root/OpenFOAM/-11/run/
