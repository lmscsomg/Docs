.. _label-1:

Tool_reStructedText_Grammar
======================

空行分段
---------
第一段内容

第二段和第一段间有空行

自动换行
--------
一个回车不分段，
本行续上行。

不留白续行
----------
行尾转义字符让\
续行之间不留白。

插入换行
---------
| 保持换行符，
| 本行不续行。


段落缩进
---------
    第一段段落缩进。

        第二段段落缩进。

    返回上一段段落缩进。

代码块
---------
::

    printf("hello world!\n");

大段代码需要指明语言类型:

.. code-block:: c++

    #include<iostream>
    using namespace std;

    int main()
    {
        cout << "test!" << endl;
        return 0;
    }


无序列表
---------
* 星号、减号、加号开始列表。

  - 列表层次和缩进有关。

    + 和具体符号无关

* 返回一级列表。

有序列表
--------
1. 数字和点是一种编写方式。

   A. 大写字母编号。

       a. 小写字母编号。

2. 继续一级列表。

   （I）大写罗马编号。

        i）小写罗编号。

列表综合
---------
1. 列表项可以拆行，
   对其则自动续行。

2. 列表项课包含多个段落。

   空行开始新的段落，
   新段落要和列表项内对齐。

3. 列表下的代码段注意对齐即可。

   ::

        printf 'hello world.'

定义
-----
git
    simple and beautiful.

subversion
    VCS with many constrains.

    Why not git ?

分隔线
------
四条或以上减号、下划线显示为分割线

-------

粗体和斜体
----------
这是 **粗体** ， 这是 *斜体* 。

不留白的\ **粗体**\ 和\ *斜体*\ 效果。

删除线
--------
.. role:: strike
   :class: strike

:strike:`删除线` 效果

不留白的\ :strike:`删除线`\ 效果

下划线
------
.. role:: ul
   :class: underline

:ul:`下划线` 效果

:不留白的\ :ul:`下滑线`\ 效果

上标和下标
-----------
- water: H\ :sub:`2`\ O
- E = mc\ :sup:`2`


等宽字体
--------
两个连续反引号内嵌代码，如: ``git status`` 。


引言
------
`RTFD`  by Victor


清除标记空白
------------
标记符号前后空白\
用\ **反斜线**\ 消除


一般方式表示表格
-----------------
+-----------+----------+------------+
| Header 1  | Header 2 | Header 3   |
+===========+==========+============+
| body row 1| column 2 | column 3   |
+-----------+----------+------------+
| body row 2| Cells may span column.|
+-----------+----------+------------+
| body row 2| haha     |  1.        |
+-----------+          |            |
| body row 3|          |  2.        |
+-----------+          |            |
| body row 4|          |  3.        |
+-----------+----------+------------+


简单方式表示的表格
-------------------

===== ==== =======
  Inputs   Output
---------- -------
  A    B   A or B
===== ==== =======
False true  False
true  true  true
===== ==== =======

URL自动链接
-------------
- 网址 http://lmsresearch.com
- email lmscsomg@gmail.com

文字链接
---------
- 访问 `Google <http://google.com/>`_ .
- 链接定义在后面，如 GitHub_ .
- 反引号括起多个单词的链接，如 `my blog`_ .

.. _Github: http://github.com
.. _my blog: http://lmsresearch.com


插入图片
----------
.. image:: me.jpg
    :scale: 50%


引用
-----
回到顶部，:ref:`label-1`

参考
-----
+ `常用轻量级标记语言对照 <http://http://www.worldhello.net/gotgithub/appendix/markups.html>`_
+ `用Sphinx编写技术文档 <http://pm.readthedocs.org/zh_CN/latest/doc/sphinx.html>`_
