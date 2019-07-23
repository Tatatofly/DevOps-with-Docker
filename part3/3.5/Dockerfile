FROM node:8-alpine as build-stage
WORKDIR /usr/app
COPY . .
RUN npm install && \
    npm run build

FROM nginx
EXPOSE 80
WORKDIR /app
COPY --from=build-stage /usr/app/dist/ /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]
