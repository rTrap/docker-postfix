FROM rtrap/debian:latest

# install apache simply from repository
RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    postfix \
    libsasl \
 && rm -r /var/lib/apt/lists/*
 
VOLUME ["/etc/postfix"]

EXPOSE 25

CMD [ "supervise", "postfix" ]
