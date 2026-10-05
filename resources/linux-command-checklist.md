# Linux 常用检查命令清单

## 进入一台机器后的第一轮检查

```bash
cat /etc/os-release
uname -a
hostname
uptime
ip -brief address
ip route
df -h
free -h
ps -ef | head
ss -lntp
```

## Git 检查

```bash
git --version
git config --global user.name
git config --global user.email
git status
```
