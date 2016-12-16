FROM debian:jessie
MAINTAINER Devops Tapioca TEAM

RUN sed -i "s/jessie main/jessie main contrib non-free/" /etc/apt/sources.list
RUN apt-get update
RUN apt-get install --yes c3270

RUN apt-get update && apt-get install --yes hercules && mkdir  /root/hercules && cd /root/hercules
COPY hercules.cnf /hercules.cnf
CMD ["hercules"]


EXPOSE 3270
