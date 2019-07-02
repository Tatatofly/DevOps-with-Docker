FROM ubuntu:16.04
EXPOSE 5000
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
COPY . .
RUN npm install
RUN npm run build
RUN npm install -g serve
ENTRYPOINT /usr/bin/serve -s -l 5000 dist
