## Changes from the original fork
Makes it so the docker-compose file works with portainer and removes the need for nginx. (Use your own reverse proxy host ex. Nginx Proxy Manger, Traefik, Apache, etc.)
All you need to do is just get your own reverse proxy and point to the IpOfContainer:5000. 
Adds Ulalou's IOS Shortcut in the footer

##

<p align="center">
  <img width="234" height="376" src="https://lolisafe.moe/xjoghu.png">
</p>

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://raw.githubusercontent.com/kanadeko/Kuro/master/LICENSE)
[![Chat / Support](https://img.shields.io/badge/Chat%20%2F%20Support-discord-7289DA.svg?style=flat-square)](https://discord.gg/5g6vgwn)
[![Support me](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dpitu%26type%3Dpledges&style=flat-square)](https://www.patreon.com/pitu)
[![Support me](https://img.shields.io/badge/Support-Buy%20me%20a%20coffee-yellow.svg?style=flat-square)](https://www.buymeacoffee.com/kana)

## What is Chibisafe?
Chibisafe is a file uploader service written in node that aims to to be easy to use and easy to set up. It's mainly intended for images and videos, but it accepts anything you throw at it.
- You can run it in public or private mode, making it so only people with user accounts can upload files as well as controlling if user signup is enabled or not.
- Out of the box support for ShareX configuration letting you upload screenshots and screenrecordings directly to your chibisafe instance.
- Browser extension to be able to right click any image/video from any website and upload it directly to your chibisafe instance.
- Chunk uploads enabled by default to be able to handle big boi files.
- API Key support so you can integrate the service with whatever you desire.
- Albums, tags and Discord-like search function
- User list and control panel

### Docker
If you want to deploy a docker instance instead of manually setting the service up, you can use `docker-composer` with our scripts. [Please refer to the docs here](docs/docker.md)

### Screenshots
<p align="center">
  <img src="https://lolisafe.moe/73up1d.png">
  <img src="https://lolisafe.moe/q0uctp.png">
  <img src="https://lolisafe.moe/8fi2x6.png">
</p>

## Author

**Chibisafe** © [Pitu](https://github.com/Pitu), Released under the [MIT](https://github.com/WeebDev/chibisafe/blob/master/LICENSE) License.<br>
Authored and maintained by Pitu. Fork by [Rapphy243](https://github.com/Pitu).

> [chibisafe.moe](https://chibisafe.moe) · GitHub [@Pitu](https://github.com/Pitu) · Github [@Rapphy243](https://github.com/Pitu)
