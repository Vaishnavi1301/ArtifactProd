FROM node:16-alpine as node
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build
#stage 2
FROM nginx:alpine
COPY --from=node /app/dist/hadiya_products_admin/ /usr/share/nginx/html
EXPOSE 80
