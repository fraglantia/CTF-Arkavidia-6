FROM ubuntu:18.04

RUN apt update && \
	apt -y install socat

RUN useradd -ms /bin/bash arkavidia

RUN mkdir /home/arkavidia/chall

COPY pakbos01 /home/arkavidia/chall
COPY flag.txt /home/arkavidia/chall
COPY run.sh /home/arkavidia/chall

EXPOSE 10099

RUN chown -R root:root /home/arkavidia/chall
RUN chmod -R 555 /home/arkavidia/chall
USER arkavidia
WORKDIR /home/arkavidia/chall

CMD ["./run.sh"]