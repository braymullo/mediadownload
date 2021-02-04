# mediadownload
Portainer Docker Compose for Media Downloaders behind a VPN with psuedo kill switch by funneling all traffic through the OpenVPN container.

modified from https://hub.docker.com/r/haugene/transmission-openvpn

list of supported VPN providers here: https://haugene.github.io/docker-transmission-openvpn/supported-providers/

Go through the MediaDownloads main stack and adjust to taste, add and remove whatever you like.

If you VPN into your Homelab you will need a Reverse Proxy set up. This is because your VPN IP is now outside of your Local range and your WEB ui ports are not accesible anymore. However port 8080 is, so hence the reverse proxy. You will now access your WEB ui's not by 192.168.x.x:port but by 192.168.x.x:8080/sonarr for exmaple. You need to enable this functionality in Sonarr, Radarr and Jackett under Settings-> General-> URL Homebase-> /sonarr

Check the included nginx.conf file for other path examples to configure your Reverse proxy.

