# Honeyd-Configs
Want to be a cyber Gemini? Try Honeyd!

**NOTE:** Honeyd isn't updated anymore. Therefore, you should use Ubuntu 12.04 LTS for it.

**Requirements:**
* nmap
* honeyd

## How to obtain personality?
```console
cat /usr/share/honeyd/nmap.assoc
```

Strings after "#" can be used in Honeyd configuration file as personality

![nmap.assoc](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/nmap.assoc.PNG)

```console
cat /usr/share/nmap/nmap-os-db | grep "Fingerprint"
```

Strings after "Personality" can be used in Honeyd configuration file as personality

![nmap-os-db](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/nmap-os-db.PNG)

### Usage
Docker image for Honeyd container: [Link](https://hub.docker.com/repository/docker/0x4f776c/imunes-honeyd)

```console
honeyd -d -f Honeyd-Configs/<personality>.conf
```

### References
[Honeyd GitHub Page](https://github.com/DataSoft/Honeyd)

[Tutorial](http://travisaltman.com/honeypot-honeyd-tutorial-part-1-getting-started/)
