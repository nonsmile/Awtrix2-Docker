# Awtrix2-Docker
Official Docker Container for [Awtrix2](https://blueforcer.de/2019/01/04/awtrix-2-0/) Host in collaboration with Blueforcer.

The Container is based on the anapsix/alpine-java:8_JDK image.

It has an autoupdate feature witch will get the latest Host from the Awtrix Site on a restart from the Container.

# Getting Started

```shell
docker run --name AwTriX2 -p 7000:7000 -p 7001:7001 -p 5568:5568/udp --restart always -e TZ=Europe/Berlin whyet/awtrix2:latest
```
# Additional Ports:

-p 80:80  For Amazon Alexa Support you need this Port. If This Port is already used this can be changed in the config file. 

# For persistent Data add:

```shell
-v pwd:/data
```

# Set Language

If you want AWTRIX to automatically display some apps like **DayOfTheWeek** in your local language/format (e.g. "Sonntag" instead of "Sunday") you can specify this with an eviroment variable.

```shell
-e JAVA_TOOL_OPTIONS="-Duser.language=zh -Duser.country=CN"
```

Where `zh` is your two-letter language code. (see [ISO 639-2](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes))  
And `CN` is your two-letter country code. (see [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2))

# IMPORTANT for Awtrix Premium Users

If you have Awtrix Premium Please run the Docker Container in Hostmode, since a rebuild of the Container is triggering a change in the hardware ID. Or deactivate the Premium license in the Interface before rebuilding.

```shell
--network host
```

# Support for Creating Docker Containers ;)

<a href="https://www.buymeacoffee.com/TechNic" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" style="height: 13px !important;width: 55px !important;" ></a>
