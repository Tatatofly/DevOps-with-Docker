FROM ubuntu:16.04
EXPOSE 8000
COPY . .
RUN apt-get update && apt-get install -y \ 
    curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    npm install && \
    useradd -m app && \
    chown -R app node_modules/ && \
    chown app logs.txt
USER app
ENV FRONT_URL=http://localhost:5000
ENV REDIS=localhost
ENV REDIS_PORT=6379
ENV DB_USENAME=docker
ENV DB_PASSWORD=docker
ENTRYPOINT npm start
