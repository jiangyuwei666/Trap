# 多个.py文件相互调用
1.要使用的应该再同一层，同一个文件夹下

2.使用之前要先导入该文件，和导包一样
</br>比如在```test.py```里面有个```class student```
```python
import test 
```
3.使用该文件中的类或者方法的时候格式应该是  文件名.方法
```python
a = test.student()
```
或者可以直接导入该类
```python
from test import student
a = student()
```