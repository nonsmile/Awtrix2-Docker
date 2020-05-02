# Awtrix2-Docker Beta Branch for ARM
Official Docker Container for Awtrix2 Host in collaboration with Blueforcer.

The Container is based on the anapsix/alpine-java:8_JDK image.

It has an autoupdate feature witch will get the latest Host from the Awtrix Site on a restart from the Container.

# Getting Started

sudo docker run --name AwTriX2 -p 7000:7000 -p 7001:7001 -p 5568:5568 --restart always -e TZ=Europe/Berlin whyet/awtrix2:latest-arm

# For persistent Data add:

-v pwd:/data

# Additional Ports:

-p 80:80  For Amazon Alexa Support you need this Port. If This Port is already used this can be changed in the config file.
