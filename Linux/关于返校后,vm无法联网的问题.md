# 关于返校后虚拟机无法联网的问题

前提:

寒假在家上了一段时间的网课,在学习linux时,在自己家中的网络环境下配置了linux网络环境,并设置为了静态IP地址,但是,没想到返校后却无法使用,自己调试一段时间后,终于成功,记录下来:


----

## 1.首先,查看你的虚拟机设置的静态IP地址:
可以在终端里输入:ifconfig进行查看,但由于我忘记截图了,直接放上我之前在设置里的截图:

<img src = https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312185450.png
width = 300px>

可以看到,我这里之前的ip静态地址是:192.168.0.109

## 2.然后,在自己电脑上查看vm8的IP地址:

(注意:我是在NAT模式下进行的,所以是vm8)

----

<font face = "隶书" size = 5 color = yellow >科普一下:可以不用看这一部分</font>

VM虚拟机常用的三种网络连接方式：分别是
<font face = "楷书" size = 3 color = red >桥接（bridge）、NAT、host-only。</font>

点击编辑虚拟机设置，在硬件选项页中，选中网络适配器，右边就出来下图

<img src =https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312190238.png 
 width = 300px>

- **桥接：就是把虚拟机通过VMnet0桥接到主机的本地连接。**

    现在虚拟机是通过VMnet0与外界联系，现在的虚拟机就相当于和主机一样是物理网络中的一台电脑，说的通俗的就是现在虚拟机就相当于和你主机同在一个网络的另一台真实的电脑。所以要想使用桥接使虚拟机上网，前提必须你的主机处在局域网中，也就是你的主机上网得有路由器，这时才能用桥接使虚拟机上网。至于虚拟机的IP设置方式和你主机一样，用不用设置IP要看你的路由器是否开启了DHCP和DNS，主机不用虚拟机也不用，主机要设置那么虚拟机也要设置。对于那些使用拨号上网方式并且没用路由器的就不要用桥接。

- **NAT：就是网络地址转换，通过VMnet8连接作为网关使虚拟机经过主机上网。**


    现在虚拟机是通过VMnet8与外界联系，说的通俗的就是在你的主机和虚拟机之间加了一个路由器，虚拟机通过这个路由器上网。NAT方式就不用考虑那么多，只要你主机能上网虚拟机就能上网，所以一般没有特殊要求推荐用NAT方式。

- **host-only：就是虚拟机和主机在一个私有网络中。**


    这时虚拟机只能和主机通讯，默认它是不能上网的。（当然不是绝对的，要想上网不过要进行另外的设置）

----

<font face = "华文宋体" size = 5 color = red >一般都使用NAT连接方式,推荐使用</font>

在cmd终端输入ifconfig查看

<img src = https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312191143.png width = 500px>

很显然与之前的虚拟机默认IP地址不在一个子网之中,因此,要清除虚拟机之前的网络配置文件,重新分配ip地址

## 3.清楚旧的网络配置,重新分配ip地址

我直接在图形化界面操作了

直接点开网络->有线->设置:

<img src = https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312191600.png
 width = 500px>

点击下面的`remove connection profile`,就可以啦

更新之后,自动获取ip地址,可以看到已经变为192.168.83.128了,然后再自己设置为静态IP即可

试试远程登陆:


![20220312192003](https://cdn.jsdelivr.net/gh/NEUQer-xing/Markdown_images/images/20220312192003.png)

成功!解决问题


