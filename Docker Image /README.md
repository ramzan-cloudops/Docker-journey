# What is Docker Image ?

A Docker image is a read-only, lightweight, and standalone template containing everything

needed to run an application, including the code, runtime, system tools, libraries, and settings.

Docker image  genratefrom the dockerfile . 

<img width="259" height="267" alt="image" src="https://github.com/user-attachments/assets/77af0f4f-bc88-499d-be8c-71f36d8d20a3" />



Here is the structured guide to understanding and creating Docker images.

- Blueprint:
  
   It acts as a static blueprint or snapshot for creating active Docker containers.

- Layered:

   It consists of multiple read-only layers stacked on top of each other.
  
- Portable:

  It runs identically on any system that supports Docker, eliminating environmental differences.

## Steps Required to Create a Docker Image 

  To create your own custom Docker image, we follow these five essential steps:

- **Set Up Your Project Directory**

  Create a dedicated folder on our computer that contains our application code, files, and dependencies.

- **Create a Dockerfile**

  In the root of your project directory, create a text file named exactly Dockerfile (with no file extension).

  This file contains the instructions Docker uses to build the image.

- **Write the Dockerfile Instructions**

  Open the Dockerfile in a text editor and define the environment.

A standard Dockerfile uses these basic commands:

 - FROM:
   Specifies the base image to build upon (e.g., FROM node:20 or FROM python:3.11).

 - WORKDIR:
   Sets the working directory inside the container.

 - COPY:
    Copies files from your local project directory into the container

  - RUN:
    Executes commands inside the container during the build phase (e.g., RUN npm install).

  - EXPOSE:
      Documents the network port the container listens on at runtime.
  
  - CMD:
     Defines the default command that runs automatically when the container starts. 

**Build the Image**   

  Open terminal, navigate the project folder, and run the docker build command. 
  
  Use the -t flag to give your image a recognizable name (tag).

  - docker build -t my-app-image:1.0 .

**Verify the Image**

  Confirm that your image was successfully created by listing all available images on your system.

  - docker images 


  

  
