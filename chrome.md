[谷歌浏览器下载](http://www.google.cn/chrome/?hl=cn&standalone=1)
#   彻底修改Google Chrome浏览器的安装目录
谷歌浏览器以其简洁的界面和快速的Javascript解析速度v8引擎，很快在浏览器市场中占有了一席之地，我们公司的绝大多数系统就建议用户选 择使用谷歌浏览器。但是说起他的安装绝对是个杯具：一是默认下载的是在线安装版的；另外一个就是默认的安装目录在系统盘，而且不能选择！！ 本文就针对这两点分别给出一个解决方案。

1.下载谷歌的离线安装包
谷歌浏览器的默认下载地址是：http://www.google.com/chrome/eula.html，其实这个地址后面可以跟很多的参数，最关键的一个参数就是standalone，将它的值设置为1就可以下载离线版了，具体的地址是：http://www.google.cn/chrome/?hl=cn&standalone=1，里面的hl是设定语言的，可以不用。

2.修改谷歌浏览器的安装目录
因为谷歌浏览器的安装程序很难进行定制，所以我们没有办法直接修改安装程序来实现修改安装目录的目的，但是可以通过一个小的技巧来制作绿色版的谷歌浏览器。

首先使用上面的方法下载离线版的谷歌浏览器，然后默认安装，安装完之后最好不要允许浏览器。谷歌浏览器的默认安装目录如下：

Win7:
C:\Users\系统用户名\AppData\Local\Google\Chrome\Application
WinXP :
C:\Documents and Settings\系统用户名\Local Settings\Application Data\Google\Chrome

进入上述目录之后，首先将chrome.exe放到包含版本号的目录中，然后将这个目录拷贝到你所想要放的地方，最后修改这个目录名就可以了，比如可以修改成GoogleChrome。

还有最后一步，就是设置UserData。可以在刚才那个GoogleChrome目录下面创建一个新的目录UserData，然后创建chrome.exe的一个快捷方式，在快捷“目标”后面加上下面的参数：

–user-data-dir=UserData

然后启动的时候直接运行这个快捷方式就可以了。

最后卸载刚才安装在系统盘下的Google浏览器就可以了。

注意几点：
1. 如果不将chrome拷贝到版本号的目录下，直接运行chrome.exe则无效；
2. 如果不在添加了–user-data-dir参数的快捷方式下运行程序，则默认情况下的User Data目录还是在系统盘下面。