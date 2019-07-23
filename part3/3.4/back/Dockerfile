FROM node:8-alpine
EXPOSE 8000
WORKDIR /app
COPY . .
ENV FRONT_URL=http://localhost:5000
ENV REDIS=localhost
ENV REDIS_PORT=6379
ENV DB_USENAME=docker
ENV DB_PASSWORD=docker
RUN npm install
ENTRYPOINT npm start
