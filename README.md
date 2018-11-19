# Communication between Docker Containers
Docker is a software container platform to run and manage apps side-by-side in isolated containers to get better compute density. A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings. Containers isolate software from its surroundings, for example differences between development and staging environments and help reduce conflicts between teams running different software on the same infrastructure. In other words, Docker containers automate deployment of applications inside software containers. Networking these containers can help create a network topology that assists in exploring additional functionalities of applications. In this project we aim to run two flask applications on docker containers which communicate with each other. These docker containers run on different LAN networks, hence network communication between two docker containers had to be established via web. It helps developed a interactive and integrated environment for our application. We  use  Docker for this purpose because it helps to build agile software delivery pipelines to ship new features faster, more securely and with confidence for both Linux and Windows Server apps.


# Docker Installation Steps:
The Docker installation package available repository may not be the latest version. To get the latest and greatest version, we need to install Docker from the official Docker repository.
 
Updating the package database:
 - sudo apt-get update
 
Add the GPG key for the official Docker repository to the system:
- sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

Add the Docker repository to APT sources:
- sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'

Update the package database with the Docker packages from the newly added repo:
- sudo apt-get update

Make to install from the Docker repo:
- apt-cache policy docker-engine

Finally, install Docker:
- sudo apt-get install -y docker-engine

Docker should now be installed, the daemon started, and the process enabled to start on boot. To check if it’s running:
- sudo systemctl status docker

# Docker Compose
Compose is a tool for defining and running multi-container Docker applications. With Compose, we can use a Compose file to configure our application’s services. Then, using a single command, we create and start all the services from your configuration.
Compose is great for development, testing, and staging environments, as well as CI workflows. 


Using Compose is basically a three-step process.
-Defining the app’s environment with a Dockerfile so it can be reproduced anywhere.
-Define the services that make up the app in docker-compose.yml so they can be run together in an isolated environment.
-Run docker-compose build
-Lastly, run docker-compose up and Compose will start and run your entire app.

# The applications are flask applications
