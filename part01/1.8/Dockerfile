FROM ubuntu:18.04

RUN apt-get update
RUN apt-get --yes install curl

WORKDIR /app

COPY fetch.sh . 
RUN chmod +x fetch.sh

CMD ./fetch.sh