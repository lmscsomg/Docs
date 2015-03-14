Linux_command_basic
===================

文件与目录管理
--------------
1. chgrp [-R] groupName fileName

   chown [-R] (groupName:)usrName fileName

   chmod [-R] 777 fileName (u,g,o,a +-)

2. pwd -p 不以连接方式显示

3. mdkir -m 777 testDir

   mkdir -p testDir/testSubDir/testFile

4. cp -a 复制全属性（权限不够无法更改）

5. cat -n 显行号

   cat -A 可列出特殊字符

6. head -n 20

   head -n -100 后100行都不打印

7. tail -n +100 打印100行以后的

   **head -n 20 fileName | tail -n 10 (第11行到第20行)**

8. SUID SGID SBIT 4 2 1

9. file 查看文件类型

10. ls -h 文件大小K或者B（就是人能看）

11. **find**

    find [PATH][option][action]

    1. 时间

           -mtime n

           -mtime +n/-n

    2. 用户

           -uid n

           -gid n

           -user name

           -group name

           -nouser/-nogroup (寻找文件所有者[组]不在/etc/passwd[/etc/group])

    3. **文件**

           -name fileName

           -size [+-]SIZE

           -type TYPE

           -perm mode

           -perm -mode

           -perm +mode(只要包含这个mode就行)

    4. find /etc -size +50k -size -60k -exec rm {}\;
    5. find /etc ! -user root -exec ls -l {}\;
    6. find /etc -size +60k || size -1k -exec ls -l {}\;

磁盘与文件系统
---------------
1. df 目录或文件名（列出文件系统整体磁盘目录）

   -h (KB MB格式)

   -i (以inode数量显示)

2. du 目录或文件名 （评估目录所占容量，默认KB）

3. ln 默认hard link

   -s symbolic link

压缩与打包
----------
1. tar 



