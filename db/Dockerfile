# ## Dockerfile ##
#
# This file describes the complete environment in which our server will run,
# including the operating system and all software dependencies. It is used
# by Docker Compose to build a Docker image for our application.

# Base this image on an official Node.js long term support image.
FROM postgis/postgis

# Install some additional packages that we need.
RUN apt-get update
RUN apt-get install gdal-bin -y
