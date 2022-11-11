# theia
This is a personal project, aim to serve my home media server with download and file management capabilities.

# Components
There are 5 main component:
- VPN container
- Download manager
- Web interface for the download manager
- File manager
- DLNA Server

## VPN Container
I'm using `bubuntux/nordvpn` image to have as the VPN container. This container will be used as a gateway for download manager.

## Download manager
This is custom image within this repository which provides a docker image with Aria2 installed and RPC configured.

## Web interface for Aria2
Another cusotme image within this repository which brings Aria2ng. Aria2ng is a web interface allows you to interact with Aria2 download manager via your browser. This is an easier way to manage the downloads.

## File manager
I'm using `filebrowser/filebrowser` image to manage the storage.

## DLNA Server
The `vladgh/minidlna` allows you to run Minidlna within a container. All the configuration are made within the image and by running it, you get the smooth experience of streaming your media.

# How to run it
The project was aimed to be used in RPI. I'm using it on a RPI4, but you can easily run it on any Linux machine. (It's not tested on Docker for Mac or Windows)

Now you need to create the `.env` file by using the example provided:
`cp .env.example .env`

TODO: Add definition for the env enteries

Then just run the following command:
```bash
docker compose up -d
```

The first time it will take some time for the image to be pulled and build.
