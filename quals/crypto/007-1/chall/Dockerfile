FROM python:2.7-alpine

RUN apk update && \
	apk add socat

RUN adduser -D -u 1001 -s /bin/bash arkavidia

RUN mkdir /home/arkavidia/chall

COPY content.txt /home/arkavidia/chall
COPY chall.py /home/arkavidia/chall
COPY run.sh /home/arkavidia/chall

EXPOSE 10099

RUN chown -R root:root /home/arkavidia/chall
RUN chmod -R 555 /home/arkavidia/chall
USER arkavidia
WORKDIR /home/arkavidia/chall

CMD ["./run.sh"]
