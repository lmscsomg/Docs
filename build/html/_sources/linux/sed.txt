Linux_sed
==========

格式
-------
sed [-nefr] [动作]

**动作:**

a 新增,在新的一行

c 替换

d 删除

i 插入,与sed -n 一起运行

p 打印

s 替换

::

    nl /etc/passwd | sed '2,5d' 将第2-5行删除

查找替换
--------
sed 's/oldString/newString/g'

**注**: newString如果为空，则相当于删除




