# Honeyd-Configs
Are you a Gemini or have you been wanting to be one? If so, try Honeyd! You will be able to double-face other systems online.

<!-- display-subdirectories: true -->

**Honeyd** is an open source program that allow users to set up and emulate virtual hosts on computer network. These v-hosts can be configured to mimic/spoof different typs of devices, operating systems, etc... allowing users to simulate an infinite number of network nodes. Honeyd is mainly used in the field of computer security and in projects such as network simulation.

**Requirements:**
* nmap (optional)
* honeyd

## How to obtain personality?

<details open>
  <summary>No Nmap? No worries!</summary>
  <p>
    
  ```console
  cat /usr/share/honeyd/nmap.assoc
  ```
    
  Strings after "#" can be used in Honeyd configuration file as personality

  ![nmap-os-db](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/nmap.assoc.PNG)
  
  </p>
</details>
  
<details>
  <summary>Nmap method</summary>
  <p>
    
  ```console
  cat /usr/share/nmap/nmap-os-db | grep "Fingerprint"
  ```
    
  Strings after "Fingerprint" can be used in Honeyd configuration file as personality
    
  ![nmap.assoc](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/nmap-os-db.PNG)
    
  </p>
</details>

## Usage

**NOTE:** Honeyd isn't updated anymore. Therefore, you should use Ubuntu 12.04 LTS for best compatibility. However, I have Docker images for both Ubuntu 12.04 LTS and Ubuntu 20.04 LTS with working copy of Honeyd. Feel free to use them!

Docker image for Honeyd container: [Link](https://hub.docker.com/repository/docker/0x4f776c/imunes-honeyd)

```console
honeyd -d -f Honeyd-Configs/<personality>.conf
```

Before executing Honeyd:

![Before](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/before-honeyd.PNG)

After executing Honeyd:

![After](https://github.com/0x4F776C/Honeyd-Configs/blob/main/screenshots/after-honeyd.PNG)

### References

[Honeyd GitHub Page](https://github.com/DataSoft/Honeyd)

[Tutorial - Linux](http://travisaltman.com/honeypot-honeyd-tutorial-part-1-getting-started/)

[Tutorial - Windows](https://www.itprotoday.com/strategy/honeyd-windows)

[Research paper on Honeyd & arpd](https://www.scitepress.org/Papers/2008/19272/19272.pdf)
