FROM node:20-alpine


WORKDIR /app


COPY package*.json .



COPY . .


RUN addgroup app && adduser -S -G app app



USER root


RUN npm install



EXPOSE 3000



USER app


CMD npm run dev





