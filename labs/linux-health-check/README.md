# Lab: Linux Health Check

## Goal

Build the habit of inspecting a Linux machine from several basic angles.

## Environment

- Debian WSL2
- User: `mwf`
- Related project repository: `~/infra-ops-lab`

## Commands

```bash
cat /etc/os-release
ip route
df -h
free -m
ps -ef | head
ss -lntp
```

## What I Am Checking

```text
OS and kernel
IP address and route
Disk usage
Memory usage
Running processes
Listening ports
```

## Result

The first `health_check.sh` script was created in `~/infra-ops-lab`.

This lab explains the thinking behind that script. The script itself belongs in the project repository, while this journal records what I learned from it.

## Follow-Up

- Add notes explaining each command.
- Run the script again after adding more checks.
- Compare manual command output with script output.
