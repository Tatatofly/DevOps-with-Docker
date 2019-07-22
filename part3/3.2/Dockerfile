FROM ubuntu:16.04
ENV LC_ALL=C.UTF-8
RUN apt-get update && apt-get install -y \
    python3 python3-pip ffmpeg wget && \
    pip3 install yle-dl && \
    rm -rf /var/lib/apt/lists/*
ENTRYPOINT ["yle-dl"]
