# 😬 cmake常用变量及配置

生成项目索引文件方法

* 在CMakeLists.txt中添加set (CMAKE\_EXPORT\_COMPILE\_COMMANDS ON)，然后在build目录下运行cmake命令，会在build目录下生成compile\_commands.json文件
* pip install compiledb && compiledb -n make -C build 两个命令
* 如果是基于Ninja方式来编译，那么可以使用ninja -c命令来生成compile\_commands.json文件



