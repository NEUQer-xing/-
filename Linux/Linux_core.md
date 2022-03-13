# Linux 内核简介

## Linux 内核

<img src =https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312173947.png width = 500px>

## Linux 内核版本

两个版本号:

    1. 测试版
    2. 发行版

注:Linux的版本号由三位数字组成`x.y.z`,<font face = "楷体" size = 3 color = red >其中第二位,也就是y说明版本类型</font>

```markmap
# 版本类型
## 偶数 = 产品化版本
## 
## 奇数 = 实验版本
```

## Linux内核目录结构

### 核心代码:

<font face = "楷体" size = 5 color = red >Linux内核源代码位于/usr/src/linux目录下</font>


linux内核目录结构

![20220312193003](https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312193003.png)

其中:
1. include/子目录包含了建立内核代码时所需的大部分包含文件
2. init/ 子目录包含了内核的初始化代码，这是内核开始工作的起点
3. arch/子目录包含了Linux支持的所有硬件结构的内核代码
4. drivers/ 目录包含了内核中所有的设备驱动程序，如块设备，scsi 设备驱动程序等
5. fs/ 目录包含所有文件系统的代码，如ext2, vfat模块的代码等。
6. net/ 目录包含了内核中关于网络的代码。
7. mm/ 目录包含了所有的内存管理代码。
8. ipc/ 目录包含了进程间通信的代码。
9. kernel/ 目录包含了主内核代码