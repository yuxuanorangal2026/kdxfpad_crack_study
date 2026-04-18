# T20_root_with_apatch-boot <br>
# 免责声明 <br>
在开始破解设备及刷机之前，您需要知悉以下几点 <br>

刷机有一定风险，有一定使设备完全损坏的可能，如果您无法保证您可以在操作之前确认您的技术不足以支持您破解此设备，或您无法保证您的设备不会因此损坏，请去淘宝或者讯飞线下店、官方维修去刷，价格保持在60~100元左右，若您执意自行操作，并因为误操作导致您的设备损坏，此文章编写团队概不负责。 <br>

如果您需要的只是安装应用功能，并要求保留学习功能，请想办法打开wanderer.rth1.xyz/iflytek.html然后你就懂了。 <br>

此文章受众：因为各种情况，以后用不上学习机学习功能并希望将此机器废物利用的用户。 <br>

未成年人请在家长允许并陪同+配合下进行刷机。如果您不同意\未获得家长允许并陪同\自认为自己技术不足的，请退出本文档，本文档部分章节已经超出了《科大讯飞AI学习机AI学习软件服务用户协议》： 用户若对学习机进行刷机行为，包括但不限于获取root权限，刷入第三方ROM等，则本机将会从科大 讯飞AI学习机官方技术支持和软件保修服务中被移除 <br>

如果您未同意此条款或者未遵守本文第四条规定并因此带来的各种经济损失，精神损失，此文章编写团队概不负责。 <br>

若您不同意以上条款，请您退出并在您的个人设备上删除此文档并不再操作 <br>
# 重大突破!目前可以刷写带有magisk的boot镜像,无需修改system,直接就有magisk了! <br>
不过你只能装一些模块,如果要装软件(系统版本过高,无法软破解时)还是得修改system
T20科大讯飞学习机通过Apatch修补boot分区的方式完成root <br>
Warning:进行Root是一项危险的操作。这将会使你的设备不再被讯飞官方的保修认可，同时，你的设备会有无法启动的风险 <br>
进行下一步视为你已经接受风险，同时自身有一定的玩机水平 <br>
# Part1.提取Boot分区 <br>
首先，你需要提取Boot分区。 <br>
如果你的设备是T20,那么可以直接使用我的boot.img,请跳到Part2继续 <br>
如果你是其他T系列(不含Pro系列，安卓系统版本必须为9）,而且芯片为Unicos(紫光展讯)，那么你可以继续阅读此教程 <br>
首先,请自行寻找并完成Sdp_dump驱动的安装，并准备好Sdp_dump深刷工具. <br>
确保你的设备已经完全关机. <br>
然后，长按音量下按键3秒钟左右，并立刻将数据线连接到电脑（此时应已打开Sdp_dump主程序exe) <br>
观察到BROM>的字样视为连接成功。 <br>
接下来，请自行寻找自己设备的fdl文件 <br>
输入loadfdl <你的fdl1文件>(注意，fdl1文件比fdl2文件小,不要打错了) <br>
如果出现了FDL1>,说明你的设备适用此教程,否则请离开 <br>
紧接着输入loadfdl <你的fdl2文件> <br>
如果Send成功,则输入exec <br>
如果不出意外，你将进入FDL2>的界面 <br>
如果失败,请检查自己的驱动或者换一根数据线 <br>
此时,输入r boot提取到自己的boot.bin <br>
将后缀名改成.img方便使用 <br>
Part1 Done! <br>
# Part2.解锁Bootloader(非常重要!) <br>
想办法进入bootloader,然后使用一键解锁BL.bat文件完成所有操作,一路Enter前进即可 <br>
Part2 Done! <br>
# Part3. 修补Boot.img <br>
下载Apatch软件或者使用在线修补,得到修补后的boot.img文件,注意此时不能刷入boot.img!!! <br>
Part3 Done! <br>
# Part4.重新签名Boot.img(非常重要,否则你的设备将无法启动!) <br>
将Resign工具Fork到你的Github Responsibility,然后在Actions中选择sign_one_partition_only <br>
类型输入boot,文件直链建议使用Airportal的 <br>
不超过5分钟你就能在Release中下载到image.img(成品修补镜像) <br>
Part4 Done! <br>
# Part5.刷入boot <br>
和第一步一样的方式进入FDL2> <br>
然后输入w boot <你的boot.img位置> <br>
看到Write Done!后执行reset进入系统 <br>
Part5 Done! <br>
# Part6.修改System <br>
进入系统后你将会十分困惑,因为桌面上并没有Apatch软件 <br>
无需担心，这是正常现象,只需要想办法安装Apatch就可以管理你已经获得的Root权限了 <br>
（未完待续) <br>
