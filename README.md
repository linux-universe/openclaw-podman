# openclaw-podman
> [!WARNING]
> **WIP**
> work in progress

##
1. clone https://github.com/openclaw/openclaw.git to `<data-path>/git` and run `systemctl start openclaw-build.service`.
2. run onboarding command as documented below
3. systemctl start openclaw-gateway.service


## run cli commands

onboarding:
```console
$ podman run --rm -e HOME=/home/node -e TERM=xterm-256color -e BROWSER=echo -v <data-path>/config:/home/node/.openclaw:z -v <data-path>/workspace:/home/node/.openclaw/workspace:z -it --init localhost/openclaw node dist/index.js onboard
```

cli commands: (gateway container needs to be running)
```console
$ podman exec -it systemd-openclaw-gateway node dist/index.js <command>
```
