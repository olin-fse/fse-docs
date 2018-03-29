## Week 9

### Docker and Containerization

Now that we're deployed to GCP, it's time to take the next step and start using Docker to bring our development and deployment workflows to the next level. 

To get started with Docker, we've laid out a set of steps we'd like you to go through before class next Monday. By the time you've gone through all of these steps you should have the following:

1. A Dockerfile that you can use to successfully create images
2. Travis building and testing against docker images as opposed to running `npm start`
3. An image of your app in DockerHub

### Suggested Steps

#### 1. [Install Docker](https://docs.docker.com/install/#updates-and-patches)

Install the Community Edition for free!

#### 2. Get a Docker ID

1. Get your [free Docker ID](https://docs.docker.com/docker-hub/accounts/)
2. Send us your username so we can add you to the Olin FSE organization.

#### 3. Walk through the Docker 'Getting Started' Tutorial

Docker offers [a tutorial](https://docs.docker.com/get-started/) to introduce some of the basic concepts of creating images, running containers, and introductions to getting networking set up. 

Go through the steps in Parts 1 and 2. 

#### 4. Familiarize yourself with the Docker documentation
The [documentation for docker](https://docs.docker.com/) is fantastic. Before you get started, poke around and learn some new things. Some pages you might want to start with are:

[Dockerfile Reference](https://docs.docker.com/engine/reference/builder/#usage)
[Dockerfile Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/#the-dockerfile-instructions)

#### 5. Write your first Dockerfile

In the root of your repository, create a file called `Dockerfile`. Figure out how to populate it. Some things you may run into include:

- Deciding on the appropriate base image to inherit from
- Defining and gathering dependencies
- Exposing and mapping ports correctly

As an exercise in navigating documentation, we're intentionally not providing specific guidance. If you get stuck, ask us for help. 

#### 6. Run your application using Docker

[Docker Build](https://docs.docker.com/engine/reference/commandline/build/)
[Docker Run](https://docs.docker.com/engine/reference/run/)

#### 7. Publish your first image to DockerHub

Check out the [Docker Hub Docs](https://docs.docker.com/docker-hub/repos/#webhooks) from Docker

You'll need configure your Docker account first. See [these docs](https://docs.docker.com/docker-cloud/builds/push-images/) for some first steps.

#### 8. Modify `travis.yml` 
Go back and make some changes to your travis config to build images and run a container using Docker. Your travis builds should now:

1. Build a docker image (hint: look into `--cache_from` to speed up the builds. Thinking about how Docker creates builds (layers), why might we want this in Travis? [Hint/Help](https://medium.com/mobileforgood/coding-tips-patterns-for-continuous-integration-with-docker-on-travis-ci-9cedb8348a62)
2. Run your E2E/integration tests against this container. 
3. Push your built images to Docker Hub. This will require some setup in Travis to make sure you have credentials set up to push. 

#### 9. Revisit your GCP Deployment

Now that we have Docker running locally, it's time to take one last step and re-think how we're deploying our application. At this point, either get docker running in your GCP Compute Engine instance by installing the necessary dependencies by SSHing in (you shouldn't need anything other than `docker`), or take the slightly easier way out and spin up a new instance from a [pre-defined VM](https://cloud.google.com/compute/docs/images#os-compute-support) from Google that has some common container application utilities pre-installed.

When you have docker installed, pull your image from Docker Hub, and use Docker run to make it do its thing. 

**This marks the end of Phase 1 of Containerization**








