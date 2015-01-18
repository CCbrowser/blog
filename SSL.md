其实软件本身具备自动导入证书的功能，在第一次启动软件的时候就执行自动导入证书到系统，但是由于每台电脑的环境不一样（例如需要管理员权限），同时个别安全类软件干扰，就会造成证书不能成功导入，直接影响https开头的网站。

例如访问YouTube、Facebook、Twitter、Gmail、Google等以https开头的网址时出现“SSL错误”，https那里有个斜杠，

<img src="https://cloud.githubusercontent.com/assets/10321405/5561063/645386ac-8df6-11e4-87c8-f28991ab1f12.jpg"/>

或者提示“该网站的安全证书不受信任”，或者页面排版混乱，这种情况都是证书没有成功导入造成的，需要自己手动导入一次证书。如果是重装了系统或者从证书管理器里删除了证书，需要再次导入。

以下是导入方法

第一步，在“local”文件夹内有一个名为“CA.crt”的文件，如果你的电脑隐藏了文件的扩展名，那么它的名字就是“CA”，它就是证书文件：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561064/64569572-8df6-11e4-8cb1-288a2591eee5.jpg"/>

第二步，双击这个“CA.crt”文件，弹出的小窗口点“安装证书”：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561065/6461f322-8df6-11e4-8355-52e6d2c7d199.jpg"/>

第三步，弹出窗口点“下一步”：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561071/6505611a-8df6-11e4-8f8a-9164a6e81dae.jpg"/>

第四步，点“将所有证书放入下列存储区”，然后点“浏览”：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561066/64660a0c-8df6-11e4-88ae-40127287e619.jpg"/>

第五步，弹出的小窗口内点“受信任的根证书颁发机构”，然后“确定”，再点“下一步”：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561067/649455f6-8df6-11e4-8560-2969ec8b5073.jpg"/>

第六步，接下来点“完成”：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561068/64a2b9ca-8df6-11e4-87ee-3084d4c92862.jpg"/>

第七步，在弹出的窗口点“是”（如果没出现下图这个安全警告，说明系统已经存在此证书）：

<img src="https://cloud.githubusercontent.com/assets/10321405/5561069/64a7048a-8df6-11e4-8c22-84ca9e5e720a.jpg"/>

第八步，提示导入成功，点“确定”，最后关闭证书窗口就可以了。

如果导入证书后还是无法访问，请重新打开浏览器，或确认系统时间是否有误，或是否没有提高系统半开连接数。
