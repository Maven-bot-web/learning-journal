# 磁盘和内存

磁盘和内存检查回答的是一个很基础的问题：这台机器现在资源够不够用。

## 查看磁盘

```bash
df -h
df -hT
```

重点字段：

```text
Filesystem   文件系统或磁盘来源
Size         总大小
Used         已使用空间
Avail        可用空间
Use%         使用率
Mounted on   挂载位置
```

在 WSL2 里，Linux 根目录所在的虚拟磁盘可能显示得很大。这不代表 Windows 已经真的占用了这么多空间，而是虚拟磁盘的上限。

## 查看内存

```bash
free -m
free -h
```

重点字段：

```text
total       Linux 能看到的总内存
used        已使用内存
free        完全空闲内存
buff/cache  用作缓存的内存
available   大致还能给程序使用的内存
```

日常判断内存是否紧张时，`available` 通常比 `free` 更有参考价值。
