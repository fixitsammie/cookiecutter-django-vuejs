# run serve local stage
FROM node:lts-alpine as build-stage
WORKDIR /app
COPY package*.json ./
RUN npm install
#COPY . .
COPY ./{{cookiecutter.frontend_project_slug}} ./
RUN npm run serve
EXPOSE 8080

# production stage
#FROM nginx:stable-alpine as production-stage
#COPY --from=build-stage /app/dist /usr/share/nginx/html
#EXPOSE 80
#CMD ["nginx", "-g", "daemon off;"]