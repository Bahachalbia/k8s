FROM node:14.5.0
RUN mkdir -p /app
WORKDIR /app
COPY package.json /app/
RUN npm install
COPY ./ /app/
EXPOSE 3001
CMD [ "npm","start"]
