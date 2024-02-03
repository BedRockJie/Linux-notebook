# 😃 交叉编译场景

查看静态库、动态库、可执行程序使用的编译工具链的GCC版本：

```bash
objdump -s --section=.comment [库或者可执行文件名称]
```

检查文件的链接库：

```
aarch64-linux-gnu-objdump -d xxx
```
