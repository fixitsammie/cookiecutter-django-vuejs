# run serve local stage
FROM node:lts-alpine as build-stage
WORKDIR /frontend

COPY ./{{cookiecutter.frontend_project_slug}} ./
RUN npm install && npm cache clean --force

ENV PATH ./node_modules/.bin/:$PATH


# production stage
#FROM nginx:stable-alpine as production-stage
#COPY --from=build-stage /app/dist /usr/share/nginx/html
#EXPOSE 80
#CMD ["nginx", "-g", "daemon off;"]