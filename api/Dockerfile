FROM debian:latest

ENV DEBIAN_FRONTEND noninteractive

WORKDIR /app

#install dep
RUN apt-get -y update
RUN apt-get -y install libssl-dev zlib1g-dev cmake g++ build-essential libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev gperf expect wget git

# build ton client
RUN git clone https://github.com/ton-blockchain/ton.git
RUN cd ton; git submodule update --init; cd ..
RUN mkdir liteclient-build

WORKDIR /app/liteclient-build
RUN cmake /app/ton
RUN cmake --build . --target lite-client
RUN cmake --build . --target fift

WORKDIR /app

RUN apt-get update -y && apt-get install python3-pip -y

COPY requirements.txt /app

RUN pip3 install -r requirements.txt

ADD fift-scripts /app/fift-scripts

RUN wget https://test.ton.org/ton-lite-client-test1.config.json

RUN mv ton-lite-client-test1.config.json ton-global.config

COPY main.py /app

EXPOSE 3000

ENTRYPOINT "/app/main.py"
