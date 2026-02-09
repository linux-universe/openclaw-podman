# openclaw-podman
> [!WARNING]
> **WIP**
> work in progress

##
1. clone https://github.com/openclaw/openclaw.git to <data-path> and run `systemctl start openclaw-build.service`.
2. run onboarding command as documented below. (`podman run --rm .... onboard`)
3. systemctl start openclaw-gateway.service


## run cli commands

```console
$ podman run --rm -e HOME=/home/node -e TERM=xterm-256color -e BROWSER=echo -v <data-path>/config:/home/node/.openclaw:z -v <data-path>/workspace:/home/node/.openclaw/workspace:z -it --init localhost/openclaw node dist/index.js <command>
```
