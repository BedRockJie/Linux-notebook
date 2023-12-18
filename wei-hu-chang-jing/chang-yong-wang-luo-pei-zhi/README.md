---
description: Linux网络命令配置
---

# 🐟 常用网络配置

## Linux ip命令使用

* 使用ip命令设置ip: `ip addr add dev enx2c16dbafcb8c local 192.168.1.12/24 broadcast 192.168.1.255`
* 删除网卡中配置的ip地址:`ip addr del dev enx2c16dbafcb8c 192.168.0.15/24`
* 启用/禁用网卡：`sudo ip link set enp0s3 up` or `sudo ip link set enp0s3 down`
* 路由，默认网关信息:`ip route show`
* 查看ARP记录:`ip neigh`
* 在缓存中添加ARP新命令：`sudo ip neigh add 192.168.0.150 lladdr 33:1g:75:37:r3:84 dev enp0s3 nud perm`

```sh
nud 的意思是 neghbour state（网络邻居状态），它的值可以是：

perm - 永久有效并且只能被管理员删除
noarp - 记录有效，但在生命周期过期后就允许被删除了
stale - 记录有效，但可能已经过期
reachable - 记录有效，但超时后就失效了
```

## 设置MAC地址

```sh
ifconfig eth1 hw ether $MAC_ADDR设置当前MAC地址
```

