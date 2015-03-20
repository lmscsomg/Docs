Linux_awk
===========

1. 基本结构
-----------
::

    awk -F '-' 'BEGIN{statements} {statements} END{statements} file'

1. -F 可选，指定分隔符

2. BEGIN/END可选

3. 顺序: BEGIN -> 每一行执行statement -> END

2. 内建变量
------------

1. NF 每一行拥有的字段总数

2. NR 目前awk做处理的是第几行数据

3. FS 目前的分隔符，默认是空格键

4. $0 当前行文本

5. $1 第一个字段

6. NF 最后一个字段


3. 例子
-------
1.

::

    $ awk -F ':' '{print $2}' fileName


2.

::

    $ awk 'NR<=3' fileName

3. 拼接字符串

::

    $ awk -F ':' '{print $1"-"$2;}' fileName

4. 统计行数

::

    $ awk 'END{print NR}' fileName

5. 过滤

::

    $ awk '$3 == 0 && $6 == "Listen"' fileName
    $ awk '$3 > 0 {print $0}' fileName

6. 字符串匹配

::

    $ awk '$6 ~ /WAIT/' fileName //第6列模糊匹配到WAIT的行
    $ awk '$6 ~ /FIN|TIME/' fileName //第6列模糊匹配FIN或者TIME
    $ awk '$6 !~ /WAIT/' fileName
    $ awk '!/WAIT/' fileName
