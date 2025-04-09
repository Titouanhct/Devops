FROM node:20-alpine
WORKDIR /app_result

COPY . /app_result
RUN npm install
EXPOSE 80
CMD [ "node", "server.js" ]

