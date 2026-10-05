# Disk And Memory

Disk and memory checks answer a simple question: does the machine have enough room and resources to work normally?

## Disk

```bash
df -h
df -hT
```

Important columns:

```text
Filesystem   The disk or virtual filesystem
Size         Total size
Used         Used space
Avail        Available space
Use%         Usage percentage
Mounted on   Where it is attached in the Linux filesystem
```

In WSL2, the Linux root filesystem may appear as a large virtual disk. This does not always mean Windows has already used that much physical disk space.

## Memory

```bash
free -m
free -h
```

Important columns:

```text
total       Total memory visible to Linux
used        Memory currently used
free        Completely unused memory
buff/cache  Memory used for cache
available   Memory likely available for applications
```

For daily checks, `available` is usually more useful than `free`.
