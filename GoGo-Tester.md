注：如果浏览器页面上出现“Over Quota”字样，那是流量没了，使用下面的方法也没有用，可以尝试刷新页面，还不行就等到美国西部24时，流量恢复后再使用。

什么样的情况可以使用以下的方法？

命令窗口出现大量的黄色警告，如图：

<img src="https://cloud.githubusercontent.com/assets/10429305/5640263/6fe8e79e-965e-11e4-87be-6e233fcfa942.png"/>

或命令窗口的“good_ipaddrs”数占总数太少，甚至出现“good_ipaddrs=0”，如图：

<img src="https://cloud.githubusercontent.com/assets/10429305/5640222/dcf445e6-965d-11e4-858e-a7964b165727.jpg"/>

（此图IP总数为50个，即good=13，bad=37，unknown=0，13+37+0=50，good_ipaddrs占总数的26%，还算可以。）

没有提高系统半开连接数的XP系统也会出现上面这种情况，请先提高系统半开连接数，然后重新启动浏览器。如果还是出现类似上图这样的情况就可以使用下面的方法来解决。（少量的黄色警告如果不影响使用，那没关系。）

以下是解决方法

先退出占用带宽的软件（例如：迅雷、网路电视、在线视频）。

打开“local”文件夹，运行“GoGo Tester.exe”（如果提示“应用程序正常初始化失败”，说明你的系统需要安装<a href="http://www.microsoft.com/zh-cn/download/details.aspx?id=17718" target="_blank">Microsoft .NET Framework 4.0</a>。），选择“随机测试”，默认获取数量为20个，为了节约时间，就以搜索3个作为演示，开始搜索。

<img src="https://cloud.githubusercontent.com/assets/10429305/5640706/2c1542dc-9664-11e4-8b0c-c3064716fe21.jpg"/>

右上角的“3”说明搜索3个IP的任务已经完成。同时点击“证书”，使证书后面出现向上的三角形，这样是将搜索到的IP排序，让有效的排在最上面，“GA”开头的是有效的、可以用的，如果有搜索到“NN”开头的那就是不能用的。

<img src="https://cloud.githubusercontent.com/assets/10429305/5642224/fd0601c6-9680-11e4-801d-10c135766463.jpg"/>

选中搜索结果中证书为“GA”开头的IP（方法一：选择排序“1”，按住“Shift”键不放，再选择排序“3”。方法二：左键点击排序“1”不放，移动到排序“3”松开左键。），按右键选择“选中的IP到用户配置文件”。

<img src="https://cloud.githubusercontent.com/assets/10429305/5641172/200015c6-966e-11e4-8c33-59e53f22ae1b.jpg"/>

成功后会弹出提示。

<img src="https://cloud.githubusercontent.com/assets/10429305/5641199/7cae8168-966e-11e4-8bcd-1a8bce04b2e7.png"/>

注意：每次使用“选中的IP到用户配置文件”都会覆盖旧的IP。如果只是想新增IP到配置文件，请右键选择导出功能复制IP，再把IP追加到“local”文件夹下的“proxy.user.ini”这个文件。

特别注意

1）部分XP系统，如果检测IP的速度很慢，请使用TCP-Z工具提高系统半开连接数。

2）软件默认一次搜索20个可用IP，你可以修改这个数值，但是把过多的IP应用到配置文件中，效果并不好。

3）“测试次数”数值越大，搜索到的IP能用的时间可能越长；越小，得到的高速IP可能越多，但不一定能久用。

4）由于防火长城的存在，我们找到的IP不可能永远有效，因此手中的IP不好使了，出现上面这种情况，那么就需要再次运行GoGo Tester这个工具，来重新寻找可用的IP。

5）每个用户的网络环境都不一样，通过自己搜索IP，可以优化网络加速效果。
