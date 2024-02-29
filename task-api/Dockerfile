FROM node:20-alpine

WORKDIR /app


COPY package*.json .


RUN npm install


COPY . .


EXPOSE 2800


RUN npx prisma generate


CMD npm run dev

