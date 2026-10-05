# Linux System Overview

When entering a Linux machine for the first time, start by identifying what the system is.

## Useful Commands

```bash
cat /etc/os-release
uname -a
hostname
uptime
```

## What To Look For

`cat /etc/os-release` shows the Linux distribution.

`uname -a` shows kernel information.

`hostname` shows the machine name.

`uptime` shows how long the system has been running and gives a quick load average.

## Current Mental Model

A Linux machine can be inspected from several angles:

```text
system -> os, kernel, hostname, uptime
storage -> disks and mounts
memory -> used and available memory
network -> IP address, route, gateway, ports
processes -> what programs are running
```
