---
description: 开发环境常用行为
---

# 🐧 系统&用户权限配置

## 系统服务管理

查看当前系统中运行的所有服务: `service --status-all`



## 系统资源管理

<pre class="language-shell"><code class="lang-shell"><strong>ps -A | grep node | awk '{print $1}' | xargs sudo kill -9 
</strong>ps -A | grep ook | awk '{print $1}' | xargs sudo kill -9 
ps -A | grep Parser | awk '{print $1}' | xargs sudo kill -9
</code></pre>

## 系统时间管理

```shell
sudo systemctl stop systemd-timesyncd.service
sudo systemctl status systemd-timesyncd.service
sudo date -s "2023-09-14"
```

## Ubuntu主板内存管理

查看内存条数目，哪个插槽的内存及对应的大小：

```bash
sudo dmidecode|grep -P -A5 "Memory\s+Device"|grep Size|grep -v Range
```

查看最大支持的内存容量

```bash
sudo dmidecode|grep -P 'Maximum\s+Capacity'
```

查看内存条上的速率

```bash
sudo dmidecode|grep -A16 "Memory Device"|grep 'Speed'
```

Windows 上查看内存条数量及支持的最大内存

```bash
# 支持的最大内存
wmic memphysical get maxcapacity
# 支持的频率情况
wmic memorychip
```
