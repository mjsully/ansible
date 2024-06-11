FROM ubuntu:22.04

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get install -y python3-pip
RUN pip3 install py3nvml
RUN pip3 install glances==3.4.0.5
RUN pip3 install prometheus_client
RUN pip3 install glances[gpu,containers,graph,ip,web]