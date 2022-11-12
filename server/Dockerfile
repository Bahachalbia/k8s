FROM node:14-alpine
WORKDIR /App
COPY ./package.json /App/
RUN npm install
COPY ./ /App/
EXPOSE 5000
CMD ["npm","start"]

