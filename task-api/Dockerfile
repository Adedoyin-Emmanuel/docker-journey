
ARG NODE_VERSION=20.11.1

FROM node:${NODE_VERSION}-alpine

ENV NODE_ENV development

ENV POSTGRES_USER admin
ENV POSTGRES_PASSWORD admin123
ENV DATABASE_URL postgresql://admin:admin123@task-api-db-1:5432/mydb?schema=public


WORKDIR /api

# Download dependencies as a separate step to take advantage of Docker's caching.
# Leverage a cache mount to /root/.npm to speed up subsequent builds.
# Leverage a bind mounts to package.json and package-lock.json to avoid having to copy them into
# into this layer.
RUN --mount=type=bind,source=package.json,target=package.json \
    --mount=type=bind,source=package-lock.json,target=package-lock.json \
    --mount=type=cache,target=/root/.npm \
    npm ci --omit=dev


RUN addgroup api && adduser -S -g api api

USER root

COPY . .

RUN npm install

EXPOSE 2800

RUN npx prisma generate

USER api

CMD npm run dev

