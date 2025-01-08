# Docker 

This repository contains a collection of ready-to-use **Docker Compose** files designed to help developers quickly set up and run various applications and development environments with minimal effort. Whether you’re spinning up a database, a full-stack web app, or other commonly used tools, these pre-configured files make the process seamless.

- [Activepieces](https://github.com/activepieces/activepieces) - True zapier alternative.
- [Healthchecks](https://docs.linuxserver.io/images/docker-healthchecks) - A watchdog for your cron jobs. It's a web server that listens for pings from your cron jobs, plus a web interface.
- [Cloudflared](https://github.com/WisdomSky/Cloudflared-web) - Cloudflare Tunnels in a Web UI
- [Dash.](https://github.com/MauriceNino/dashdot) - A simple, modern server dashboard, primarily used by smaller private server
- [Dockge](https://github.com/louislam/dockge) - Docker compose.yaml stack-oriented manager.
- [Dozzle](https://github.com/amir20/dozzle) - Dozzle is a small web based app to monitor Docker logs
- [Duplicati](https://github.com/linuxserver/docker-duplicati) - Store securely encrypted backups in the cloud!
- [File Browser](https://github.com/filebrowser/filebrowser) - Access your homeserver files from your browser
- [Firefly III](https://github.com/firefly-iii/firefly-iii) - Firefly III: a personal finances manager 
- [Grafana](https://github.com/grafana/grafana) - The open and composable observability and data visualization platform
- [Homarr](https://github.com/ajnart/homarr) - Homarr is a simple and lightweight homepage for your server, that helps you easily access all of your services in one place.
- [Home Assistant](https://github.com/home-assistant/core) - Open source home automation that puts local control and privacy first
- [Jellyfin](https://github.com/jellyfin/jellyfin) - A media server for your home collection
- [MongoDB](https://github.com/mongodb/mongo) - MongoDB is an open-source NoSQL database
- [Nextcloud](https://github.com/nextcloud/server) - Productivity platform that keeps you in control
- [Nginx](https://github.com/nginx/nginx) - Open-source simple and fast web server.
- [Pi-hole](https://github.com/pi-hole/pi-hole) - A black hole for Internet advertisements
- [Plex](https://github.com/plexinc/pms-docker) - Stream Movies & TV Shows
- [Portainer](https://github.com/portainer/portainer) - Making Docker and Kubernetes management easy.
- [Scrypted](https://github.com/koush/scrypted) - High performance home video integration and automation platform
- [Tailscale](https://github.com/tailscale/tailscale) - The easiest, most secure way to use WireGuard and 2FA.
- [Uptime Kuma](https://github.com/louislam/uptime-kuma) - A fancy self-hosted monitoring tool.
- [VaultWarden](https://github.com/dani-garcia/vaultwarden) - All your passwords in your control!
- [Wireguard](https://github.com/WeeJeWel/wg-easy/) - VPN server for your homeserver

## Volume

Before you run the Docker Compose file, you need to specify the volume path for the container. The volume path is the location where the container will store its data. You can specify the volume path in the `.env` file.

For example, to specify the volume path for the `nextcloud` container, you can add the following line to the `.env` file:

```bash
VOLUME_PATH=/mnt/docker/nextcloud
```

## Network

To create a named Docker network for containers, specify the network name and options in the `docker-compose` file. 

For example:

```yaml
networks:
  default:
    name: nextcloud
    driver: bridge
```

> By defining the default network, all services in the Compose file will use this network unless explicitly assigned to another one.

## Time Zone and PUID/PGID

In some cases, you may need to specify the time zone and PUID/PGID for the container.

You can specify the time zone and PUID/PGID for the container in the `.env` file. The time zone is the location where the container will run, and the PUID/PGID is the user ID and group ID of the container.
