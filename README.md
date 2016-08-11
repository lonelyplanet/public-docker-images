# Docker Images

A collection of Dockerfiles and related code for building Docker Images.

## Important Notes

* it should be used only for public images
* images created here should be pushed to the [lonelyplanet](https://hub.docker.com/r/lonelyplanet/) organization on Docker Hub and made public
* at the same time those images should be pushed to ECR, this way we'll be able to reuse them for local development and for running in AWS

## Images
Each image has it's own directory

## Tips

* If you need to share the same Docker image between multiple services, consider adding it to this repository
* Same rules apply in case you have some common parts between multiple images
* Extracting common stuff into separate image will optimize build and deployment speed because we avoid repeating the same steps every time when we build image for the specific service
* Currently you will have to push it manually to Docker Hub and to ECR every time you make any changes
* We don't have optimize for image size, but it's good idea to keep the images slim
* It's better to optimize for readability or maintainability, so for example you can use `ubuntu` over `alpine` as your base image