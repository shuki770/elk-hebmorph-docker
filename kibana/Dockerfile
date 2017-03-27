FROM kibana:4.6
MAINTAINER Ory Band <oryband@gmail.com>

# netcat is necessary for waiting for elasticsearch
# to be ready
RUN apt-get update && apt-get install -y netcat && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY entrypoint.sh /tmp/entrypoint.sh

CMD ["/tmp/entrypoint.sh"]
