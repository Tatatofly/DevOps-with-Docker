FROM node:8-alpine
EXPOSE 5000
WORKDIR /app
COPY . .
ENV API_URL=http://localhost:8000
RUN npm install -g serve && \
    npm install && \
    npm run build
ENTRYPOINT /usr/local/bin/serve -s -l 5000 dist
