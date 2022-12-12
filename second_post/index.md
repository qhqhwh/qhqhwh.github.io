# 在虚拟机中安装Linux



# 使用vmware workstation pro 安装并连接Linux
## 1.准备工作
### (1)下载并安装好vmware workstation pro（实验室已经安装好，可以在windows菜单中搜索vmware打开）

### (2)下载linux安装镜像文件（有点大，15.6G，实验室已经下载好，在D:\linux_os\installer目录下）：https://repo.openeuler.org/openEuler-22.03-LTS/ISO/x86_64/openEuler-22.03-LTS-everything-x86_64-dvd.iso

## 2.新建虚拟机
### (1)点新建虚拟机，选Linux，版本选其他Linux3.x 64位（如果有“其他Linux4.x 64位”的话，选4.x这种高版本的）

### (2)名称可以自己修改，位置可以修改到一个空间足够的地方

<image src="/14.jpeg">

### (3)CPU用默认的，如果物理机CPU够的话，可以多分配一些

<image src="/15.jpeg">

### (4)内存至少1024M，物理机够的话，可以多分配

<image src="/16.jpeg" >

### (5)网络类型用默认的NAT

<image src="/17.jpeg">

### (6)选默认
 
<image src="/18.jpeg"> 
 
### (7)选默认

<image src="/19.jpeg">

### (8)默认

<image src="/20.jpeg">

### (9)磁盘大小可以设置大一点，这里80G（但实际是用了多少，就占用多少，不是直接占用80G）

<image src="/21.jpeg">

### (10)用默认的不用改：

<image src="/22.jpeg">

### (11)点“完成”

<image src="/23.jpeg">

## 3.设置安装镜像文件
### (1)点设置：

<image src="/24.jpeg">

### (2)点CD/DVD，选择“使用ISO映像文件”，点“浏览”选择之前下载的openeuler镜像文件（openEuler-22.03-LTS-everything-x86_64-dvd.iso），点“确认”保存

<image src="/25.jpeg">

## 4.设置网络
### (1)打开虚拟网络编辑器

<image src="/26.jpeg">

### (2)（如果界面是操作不了，先点右下角中的“更改设置”按钮）确保VMnet1为“仅主机模式”，并且勾选了图中框出的两个选项

<image src="/27.jpeg">

### (3)回到设置中，点“添加”

<image src="/28.jpeg">

### (4)选“网络适配器”

<image src="/29.jpeg">

### (5)将网络适配器2改成自定义模式，并选中VMnet1

<image src="/30.jpeg">

### (6)开启虚拟机

<image src="/31.jpeg">

## 5.在虚拟机中安装Linux
### (1)到菜单选择界面，按方向键，选中“Install openEuler”（白色为选中状态），按回车键

<image src="/32.jpeg">

### (2)选“中文”

<image src="/33.jpeg">

### (3)点安装目的地

<image src="/34.jpeg">

### (4)直接点完成

<image src="/35.jpeg">

### (5)软件选择

<image src="/36.jpeg">

### (6)选“服务器”，右边勾上“Linux的远程管理”，然后点完成

<image src="/37.jpeg">

### (7)网络和主机名

<image src="/38.jpeg">

### (8)分别选中两个网卡，打开两个网卡的开关

<image src="/39.jpeg">

### (9)分别选中两个网卡，点“配置”，在“常规”中，两个网卡都勾选上“自动以优先级连接”，点保存

<image src="/40.jpeg">

### (10)改一下主机名，改成euler，点应用，然后点完成

<image src="/41.jpeg">

### (11)点根密码

<image src="/42.jpeg">

### (12)设置root用户的密码，至少包含大写字母、小写字母、数字、符号中3种（要记好，别忘记了！后面经常要用的），点完成

<image src="/43.jpeg">

### (13)点创建用户

<image src="/44.jpeg">

### (14)输入用户名、密码，密码中不能包含用户名

### (15)勾上“将此用户设为管理员”！

### (16)点“完成”，然后点“开始安装”

<image src="/45.jpeg">

### (17)等待安装完成后，点重启系统。

<image src="/46.jpeg">

### (18)重启后进入Linux系统，输入用户名，密码（注意输入的密码不会回显！输入正确的密码后回车即可，如果密码输入错误，需要等待几秒再重新输入用户名、密码）

<image src="/47.jpeg">

## 6.使用Tabby远程连接到Linux
### (1)在Linux中输入命令ip address，记住enp0s8网卡（可能是其他网卡名，试下哪个网卡的IP可以在Windows上ping通）对应的ip地址，比如我这里的192.168.56.117（每个人的电脑可能不一样）

<image src="/48.jpeg">

### (2)在windows上安装tabby，安装包可以从官网下载：https://tabby.sh/

### (3)安装好后打开tabby的设置

<image src="/49.jpeg">

### (4)新配置，选择SSH连接

<image src="/50.jpeg">

### (5)填入配置名、刚刚记住的IP地址、用户名（安装Linux时创建的用户名）、选“密码”身份验证方法，设置密码（安装Linux时设置的密码），保存

<image src="/51.jpeg">

### (6)点这个按钮

<image src="/52.jpeg">

### (7)选择刚刚创建的配置（比如我这里的openeuler22.03）

<image src="/53.jpeg">

### (8)接受并记住

<image src="/54.jpeg">

### (9)以后每次开好虚拟机后，就可以通过tabby远程连接到Linux，对Linux进行操作。

<image src="/55.jpeg">


