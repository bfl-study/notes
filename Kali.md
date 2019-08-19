## kalilinux的图形界面和文本界面的切换
### 文件修改开机是否图形配置：

    1 配置图行界面的文件是 vi /etc/default/grub
    找到：GRUB_CMDLINE_LINUX_DEFAULT="quiet"，应该是在第11行。
    复制本行然后把quiet替换成text。
    把本行注释掉（以免以后想改回来时不知道怎么改回来）。
    保存后 执行sudo update-grub命令后 重启即可

    2 如果想kali每次启动是文本模式可以修改如下文件：
    vi /etc/X11/default-display-manager
    把里面内容/usr/sbin/gdm3改为false之后重启会以文本模式登录，想改回图形就把false还原回/usr/sbin/gdm3
