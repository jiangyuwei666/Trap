# Pycharm不能导入第三方库？
问题是这样发生的:
</br>我是直接用Anaconda直接装的Python3.6
</br>因为爬虫需要很多库都在里面，直接一键全部安装
</br>安装完成了pycharm的时候就想试试环境是否搭建好了导入了requests库
```python
from lxml import etree
#这是对网页XML结构进行解析的模块
```
可是发现报错了，导不进去，刚开始以为是没有装这个模块
</br>到cmd里去下载

![cmd下载lxml](https://github.com/jiangyuwei666/Trick/blob/master/pic/cmd%E4%B8%8B%E8%BD%BDlxml.png)

显示的已经安装了,只是叫我更新Anaconda，怀疑是Python没有安排上
</br>又去检查Python

![检查Python](https://github.com/jiangyuwei666/Trick/blob/master/pic/%E6%A3%80%E6%9F%A5python.png)

而且发现lxml也能导入

最后排查出来是Python的路径没有放对

![Python路径检查](https://github.com/jiangyuwei666/Trick/blob/master/pic/python%E8%B7%AF%E5%BE%84.png)

这里我们创建这个项目的时候，不知道什么原因它重新在一个目录里创建了一个python？显示是这么显示的。
</br>而且我记得以前创建一个项目的时候里面是什么东西都没有，现在多了个这个东西

![多的文件](https://github.com/jiangyuwei666/Trick/blob/master/pic/%E5%A4%9A%E7%9A%84%E6%96%87%E4%BB%B6.png)

最后在正确的导入了Python后，打开的项目是这样的

![正常情况](https://github.com/jiangyuwei666/Trick/blob/master/pic/%E6%AD%A3%E5%B8%B8.png)

所以第一次使用Pycharm的时候出现这种错误的时候可以检查一下python的路径是否放对了