# Pycharm的安装
上一次装Pycharm还是大一的上学期,重装了个系统，毕竟已经一年多了完全不记得上次是怎么装上的,今天打开居然要收费我肯定是不会让他的阴谋得逞的,于是开始百度。
1. 我先直接去搜索注册码然后找得到了这个网址[http://idea.lanyus.com/]
![](https://github.com/jiangyuwei666/Notes/blob/master/pictrue/pycharm2.png)
接着我就直接贴上验证码以为就完了,然后就这样了
![](https://github.com/jiangyuwei666/Notes/blob/master/pictrue/pycharm1.png)
2. 发现还要修改一个文件
[C:\Windows\System32\drivers\etc]里面的hosts文件中加入
```
0.0.0.0 account.jetbrains.com
```
</br>这是用来屏蔽pycharm的验证的
</br>不能用txt打开,因为一保存就不知道保存到哪去了(我的文档),所以我直接用了一手vscode成功修改

3. 接着再添加一下注册码就直接安排上了