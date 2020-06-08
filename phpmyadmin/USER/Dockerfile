FROM ubuntu

RUN groupadd -r mygrp && useradd -r -g mygrp myuser

USER root
ARG DEBIAN_FRONTEND=noninteractive

USER myuser:mygrp
RUN apt-get install -y apache2 

RUN apt-get update

EXPOSE 9090
