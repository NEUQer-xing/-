# 管道和vi编辑

## 管道

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312235433.png " width = 500px>

例如:

cat /etc/passed | grep xc

意思就是在passed的文件中寻找xc关键字

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312235833.png " width = 500px>

## vim编辑器

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313083554.png " width = 500px>

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313084032.png " width = 500px>
<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313084049.png " width = 200px>

- 常用快捷键
  - 
    - 命令模式

        |快捷键|功能|
        |----|-----|
        |/关键字|从上往下搜索|
        |？关键字|从下往上搜索|
        |n |定位搜索到的下一个内容|
        |N |定位搜索到的上一个内容|

    - 底线模式

        |快捷键|功能|
        |---|---|
        |:wq!| 保存并退出|
        |:w |保存|
        |:q!| 强制退出(不保存)|
        |:set nu |显示行号|
        |:set nonu |不显示行号|
        |:行号|跳转到指定行|


# Linux用户与权限

## useradd命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313085011.png " width = 500px>

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313085150.png " width = 500px>

## passwd命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313085245.png " width = 500px>

## userdel命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313085332.png " width = 500px>

例如:

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313085426.png " width = 500px>

## id命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313090147.png " width = 500px>

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313090243.png " width = 500px>

## Linux文件权限
### 查看文件权限
<font face = "宋体" size = 5 color = skyblue >**ls -l [文件名]**</font>

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313090945.png " width = 500px>

例如: 以etc目录为例:
- d :文件类型
   -
  - I : 链接文件
  - d : 目录
  - -:文本文件
- rwxr-xr-x: 文件权限
  - 
  - 前三个: rwx 文件所有者的权限 可读 可写 可执行文件
  - 中间三个:r-x 文件所有者同组用户权限 可读 不可写 可执行
  - 后面三个:r-x 其它用户权限 可读 不可写 可执行
- 2: 硬链接数
  - 
- root: 文件所有者
  -   
- root: 文件所有者所在组
  - 
- 6 :文件大小
  - 
### chmod命令
<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313091811.png " width = 500px>

### chown命令
<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313091851.png " width = 500px>

### usermod命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313091930.png " width = 500px>

### su命令

<img src = "https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220313092006.png " width = 500px>




