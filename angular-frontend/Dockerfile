FROM node:latest as builder
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod

FROM nginx:alpine
COPY --from=builder /app/dist/my-app /usr/share/nginx/html