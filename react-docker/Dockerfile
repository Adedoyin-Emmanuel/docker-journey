# We're getting node version 20 from the alpine linux
FROM node:20-alpine


# We're setting out working directory to /app
WORKDIR /app


# We copy the package.json and package.lock files
COPY package*.json .


# We copy the rest of the files

COPY . .


# We add a new group and a new user
RUN addgroup app && adduser -S -G app app



# We change the user to the root user for admin privileges
USER root


# We install our project dependencies
RUN npm install



# We expose out app to a certain port, typically 3000 for vite
EXPOSE 3000



# Run out project
CMD npm run dev





