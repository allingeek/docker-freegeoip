#docker-freegeoip

A Dockerfile for downloading and deploying the most recent version of https://github.com/fiorix/freegeoip. No quota restrictions enabled. License applies to the Dockerfile alone and should not translate to any software downloaded or executed during use.

##Installation
Deploying freegeoip is a breeze with Docker, our only direct and on-box dependency. If you haven't already go get started at https://www.docker.io/gettingstarted/#h_installation.

Once Docker is installed on your host machine, clone this repo locally and build the docker image:

	git clone git@github.com:allingeek/docker-freegeoip.git
	cd docker-freegeoip
	sudo docker build .

##Fire It Up
Once you've build the image locally, you'll want to pull the generated image ID using:

	sudo docker images

Alternatively, you may have specified the -t option duing build to tag the resulting image for ease of reference later.
Starting the service using Docker, replace <BARE-HOST-PORT> with the actual TCP port number you want to run the service on:

	sudo docker run -d -p <BARE-HOST-PORT>:8080 <GENERATED IMAGE ID>

