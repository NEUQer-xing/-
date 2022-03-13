# Linux命令: 基础命令 + 文件管理命令

## Linux 基础命令

### Linux 命令格式

<table><tr><td bgcolor = yellow ><font face = "楷体" size = 5 color = red >常见的Linux命令格式:

命令名称 [命令参数] [命令对象]</font></table></tr></td>

- 命令参数普遍以`-`,`--`为前缀
- 命令对象一般指需要处理的文件,目录,用户等资源
- 命令参数分为长格式与短格式:
  - 长格式: ls --all  -- + 单词
  - 短格式: ls -a     - + 单词首字母

### man 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312200542.png " width = 500px>

比如:
```linux

man java

目的:输出有关java的命令帮助信息

```

结果:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201146.png " width = 500px>

### cd命令

cd命令比较熟悉了:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201312.png " width = 500px>

### pwd命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201350.png " width = 500px>

比如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201510.png " width = 500px>

### ls 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201604.png " width = 500px>


例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312201736.png " width = 500px>

---

<font face = "楷书" size = 5 color = red >注意:</font>

ls -d 只会显示当前文件夹

ls -ld 只会显示当前文件夹的信息

例:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312203129.png " width = 500px>

----

注: Linux目录结构 是典型的树形文件结构
|目录|说明|
|--|--|
|/|根目录，一切路径的起点|
|/bin| 可执行文件，如用户命令|
|/var |可变文件|
|/dev |设备文件|
|/home |普通用户home目录|
|/lib |库文件，内核模块文件|
|/root |root用户home目录|
|/proc| 虚拟文件系统，内核映射文件|
|/opt |第三方软件|
|/sys |虚拟文件系统，设备相关映射文件|
|/sbin |重要的系统执行文件|
|/usr |继承于UNIX，存放程序与相关数据|
|/boot |系统启动相关文件|

## Linux 文件管理

### mkdir 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312203739.png " width = 500px>
<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312203911.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312204148.png " width = 500px>

其实,-p参数,就是当要创建的文件夹的上一级文件夹不存在时,直接创建上一级文件夹


### touch 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312204756.png " width = 500px>

例1:创建空白文本文件 

<font face = "宋体" size = 3 color = red >在Linux系统中,文本文件是没有后缀名的</font>

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312205431.png " width = 500px>

将文件拖到window系统下,查看其属性:也没有

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312205523.png " width = 500px>

如果直接创建有.txt的:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312205814.png " width = 500px>

<font face = "宋体" size = 3 color = yellow >注意:在Linux系统中,文件名就是0312.txt,并不是后缀名</font>

而在windows系统中,直接识别为.txt文件

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312210045.png " width = 500px>

### rm 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312210701.png " width = 500px>

### cat 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312222953.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312223458.png " width = 500px>


### more 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312223628.png " width = 500px>

----
<font face = "楷体" size = 5 color = green >cat和more的区别</font>

- cat作用：

    连接并显示指定的一个或者多个文件的有关信息

    使用方式：cat[选项]文件1 文件2 ...

    -n:由第1行开始对所有输出的行号编号

    -b:和-n一样不过对于空白行不编号

    列子：cat -n hello.c hello1.c

- more作用：

    类似cat，不过会以一页一页的显示方便使用者一页页阅读

    使用方法：more [选项] 文件名

    例子：more -s testfile 逐页显示testfile内容，有连续两行以上空白行则以一行空白行显示

    more +30 testfile 从第30行开始显示testfile内容

----

### head 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224110.png " width = 500px>

### tail 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224151.png " width = 500px>

### cut 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224234.png " width = 500px>

### wc 命令 == word count

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224359.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224547.png " width = 300px>

### diff 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312224813.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312225256.png " width = 500px>

### stat 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312225813.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312230203.png " width = 500px>

### file 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312230252.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312230401.png " width = 500px>

### find 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312230706.png " width = 500px>

例如:

- find / -name passed

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312231103.png " width = 500px>

- find / -user xc


文件特别多


<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312231259.png " width = 500px>

----

<font face = "楷体" size = 5 color = red >* 通配符的使用</font>

例子如下:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312233021.png " width = 500px>

---

### grep 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312233221.png " width = 500px>

### tar 命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312233320.png " width = 500px>

### zip/unzip命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312233354.png " width = 500px>




