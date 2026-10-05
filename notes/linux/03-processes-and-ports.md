# Processes And Ports

Processes show what is running. Ports show what is listening for network connections.

## Processes

```bash
ps -ef
ps -ef | head
```

Important columns:

```text
UID    User running the process
PID    Process ID
PPID   Parent process ID
CMD    Command that started the process
```

## Listening TCP Ports

```bash
ss -lntp
```

Common options:

```text
-l  listening sockets
-n  numeric addresses and ports
-t  TCP sockets
-p  process information
```

This command helps answer: what network services are open on this machine?
