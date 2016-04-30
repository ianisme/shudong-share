# 树洞外链
树洞外链是一款免费开源的PHP外链网盘系统，界面简洁友好，支持七牛、本地、远程三种储存方式，支持多用户系统。
#安装
##环境要求
PHP版本>=5.3且启用Mysqlnd 
MySQL>=5.1
##安装过程
未安装会自动跳转的安装目录，按照提示安装
#许可
代添加
#作者
E-mail:abslant@126.com

# 远程服务器调用方法：
## PHP版服务端脚本
不推荐使用这种方式，推荐使用以后更新的Python脚本。。。

下载地址：http://wangpengnimei.ctfile.com/fs/7zR149909465

下载后传到服务端，后面自己领悟吧

## Python版服务端脚本

Python版脚本更稳定，理论上可上传无限大的文件（PHP文件大小有限制）,所以我更推崇这种服务端。

安装说明：

我将以举例的方式说明Python版服务端安装.

1.首先要在服务器上安装Python，推荐2.7版本，其他版本未做兼容性测试。教程大家可以百度

2.安装pip(已安装可以跳过)
下载Python脚本：http://wangpengnimei.ctfile.com/fs/N5R149909534
并再终端中运行即可自动下载安装。

3.安装Flask(已安装可以跳过)
执行以下命令自动安装：

```
sudo
install Flask
```

4.比如我有个剩余空间很大的服务器，已经装好了Nginx或其他服务器软件（这是必须的）,绑定的域名是f.aoaoao.me，
网站目录位于/home/wwwroot/default/下。而我想把文件都传到网站的data目录下，并以http://f.aoaoao.me/data/文件名 的形式外链出去。下面就以这种情形说明服务端的配置
先在/home/wwwroot/default/目录下创建data目录。

然后把下面的脚本保存为fileServer.py
http://wangpengnimei.ctfile.com/fs/90r149909630

打开树洞外链的后台，添加上传方案，把自动生成的Token复制下来并填到脚本第13行，保存，然后使用其他方式比如ftp，上传到/home/wwwroot/目录下（注意不要传到default目录下，否则有安全隐患）

然后把终端切换到wwwroot目录，并运行脚本

如果看到下面提示，说明脚本运行成功了

其中的8000是默认的服务端端口，如果被占用可以在第97行更改。

验证外网是否能访问，打开f.aoaoao.me:8000如果出现下面提示，就表示远程端口部署成功：
![](https://o2d4gc37w.qnssl.com/wp-content/uploads/2016/02/QQ%E6%88%AA%E5%9B%BE20160213154433-1.png)
然后上传方案的配置例子：
![](https://o2d4gc37w.qnssl.com/wp-content/uploads/2016/02/360%E6%88%AA%E5%9B%BE20160213154949992.jpg)


