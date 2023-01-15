FROM node:18 AS builder
COPY . /app
WORKDIR /app
RUN yarn && yarn build
FROM nginx
COPY --from=builder /app/dist/front/ /usr/share/nginx/html
