# 😉 Windows编译Opencv记录

Windows环境中使用Clion中的工具链来编译Opencv，方便又快捷。

编译过程会报错，错误解决参考链接：[https://github.com/opencv/opencv/issues/23070](https://github.com/opencv/opencv/issues/23070)

过程需要增加一些配置：

* OPENCV\_DOWNLOAD\_MIRROR\_ID 变量设置为 gitcode
* 关闭 Java 和 Python 的使能
* 关闭 WITH\_OBSENSOR 的使能

然后使用Ninja编译即可。
