# React + Docker V2 🚀

In this directory, I'm going to **Dockerize** a **React-App**. But this will be different from the rest, I will be using the **Docker** `init` and the **Docker** `compose` to run the images. Also I will've a **compose.yaml** file which is the most important part of the **Docker** `compose`. This is what we will use to define multiple services for example in the **API** project. Using the **Docker** init, provides us with basic configuration and basic images we will need based on our project.

## Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at <http://localhost:3000>.

## Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

## References

- [Docker's Node.js guide](https://docs.docker.com/language/nodejs/)
