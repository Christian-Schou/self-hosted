# Awesome Stacks 🔥

Deploy 90+ open-source web apps with one Docker command. 🥳

## Features ✌️

- [x] Traefik compatibility
- [x] Portainer compatibility
- [x] No need to manage configuration files
- [x] Distributed storage compatibility (GlusterFS, Ceph, NFS) with the env `VOLUME_PATH=/mnt/storage_mountpoint/`

## Get started 🚀

```bash
# 1. Deploy traefik
docker swarm init
docker network create --driver=overlay traefik-net
docker stack deploy -c stacks/traefik.yml traefik

# 2. Check your HTTP and HTTPS ports
curl https://ipv4.am.i.mullvad.net/port/80
curl https://ipv4.am.i.mullvad.net/port/443

# 3. Deploy a stack
DOMAIN=<yourdomain.com> docker stack deploy -c <stack.yml> <name>

# Example
DOMAIN=blog.christian-schou.dk docker stack deploy -c stacks/ghost.yml ghost-twc
```

## Support me 💰

I'd love to work on this project, but my time on this earth is limited, support my work to give me more time!

Please support me with a one-time or a monthly donation and help me continue my activities.

[![Github sponsor](https://img.shields.io/badge/github-Support%20my%20work-lightgrey?style=social&logo=github)](https://github.com/sponsors/Christian-Schou/)
[![Github](https://img.shields.io/github/followers/Christian-Schou?label=Follow%20me&style=social)](https://github.com/Christian-Schou)

## License

This project is licensed under the GNU GPL v3.0 - see the [LICENSE.txt](https://raw.githubusercontent.com/ethibox/awesome-stacks/master/LICENSE.txt) file for details

**Free Software, Hell Yeah!** 🙌
