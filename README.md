# T20_root_with_apatch-boot-
T20科大讯飞学习机通过Apatch修补boot分区的方式完成root
Warning:进行Root是一项危险的操作。这将会使你的设备不再被讯飞官方的保修认可，同时，你的设备会有无法启动的风险
进行下一步视为你已经接受风险，同时自身有一定的玩机水平
Part1.提取Boot分区
首先，你需要提取Boot分区。
如果你的设备是T20,那么可以直接使用我的boot.img,请跳到Part2继续
如果你是其他T系列(不含Pro系列，安卓系统版本必须为9）,而且芯片为Unicos(紫光展讯)，那么你可以继续阅读此教程
首先,请自行寻找并完成Sdp_dump驱动的安装，并准备好Sdp_dump深刷工具.
确保你的设备已经完全关机.
然后，长按音量下按键3秒钟左右，并立刻将数据线连接到电脑（此时应已打开Sdp_dump主程序exe)
观察到BROM>的字样视为连接成功。
接下来，请自行寻找自己设备的fdl文件
输入loadfdl <你的fdl1文件>(注意，fdl1文件比fdl2文件小,不要打错了)
如果出现了FDL1>,说明你的设备适用此教程,否则请离开
紧接着输入loadfdl <你的fdl2文件>
如果Send成功,则输入exec
如果不出意外，你将进入FDL2>的界面
如果失败,请检查自己的驱动或者换一根数据线
此时,输入r boot提取到自己的boot.bin
将后缀名改成.img方便使用
Part1 Done!
Part2.解锁Bootloader(非常重要!)
想办法进入bootloader,然后使用一键解锁BL.bat文件完成所有操作,一路Enter前进即可
Part2 Done!
Part3. 修补Boot.img
下载Apatch软件或者使用在线修补,得到修补后的boot.img文件,注意此时不能刷入boot.img!!!
Part3 Done!
Part4.重新签名Boot.img(非常重要,否则你的设备将无法启动!)
将Resign工具Fork到你的Github Responsibility,然后在Actions中选择sign_one_partition_only
类型输入boot,文件直链建议使用Airportal的
不超过5分钟你就能在Release中下载到image.img(成品修补镜像)
Part4 Done!
Part5.刷入boot
和第一步一样的方式进入FDL2>
然后输入w boot <你的boot.img位置>
看到Write Done!后执行reset进入系统
Part5 Done!
Part6.修改System
进入系统后你将会十分困惑,因为桌面上并没有Apatch软件
无需担心，这是正常现象,只需要想办法安装Apatch就可以管理你已经获得的Root权限了
（未完待续)
