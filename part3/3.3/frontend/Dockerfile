FROM ubuntu:16.04
EXPOSE 5000
COPY . .
RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    npm install && \
    npm install -g serve && \
    npm run build && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app node_modules/
USER app
ENV API_URL=http://localhost:8000
ENTRYPOINT /usr/bin/serve -s -l 5000 dist
