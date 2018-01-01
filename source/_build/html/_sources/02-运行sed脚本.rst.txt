02 运行sed脚本
============================================

2.1 预览
----------------------------------

正常情况下。sed是这样使用的。

.. code-block:: bash

    sed SCRIPT INPUTFILE...

样例1-替换

.. code-block:: bash

    #替换hello文本为world文本
    sed 's/hello/world/' input.txt > output.txt

样例2-修改文件

.. code-block:: bash

    #替换hello文本为world文本,这个会直接修改output.txt的文件的。
    sed -i 's/hello/world/' input.txt > output.txt

样例2-处理指定的行

.. code-block:: bash

    #只打印第45行
    sed -n '45p' input.txt > output.txt


2.2 命令行选项
----------------------------------

全格式的sed命令格式是这样的：
 
.. code-block:: bash

    sed OPTION... [SCRIPT] [INPUTFILE...]

命令行参数如下

--version                   版本信息
--help                      帮助信息
-n                          禁用自动打印
--quiet                     禁用自动打印
--silent                    禁用自动打印
-e                          添加命令
--exoression                添加命令
-f                          命令指定在文件里面
--file                      命令指定在文件里面
-i                          替换文件
--in-place                  替换文件                       
--posix                     posix sed
-b                          二进制处理
--binary                    二进制处理
--follow-symlinks           追踪符号链接文件
-E                          扩展正则
-r                          扩展正则
--regexp-extended           扩展正则
-s                          替换
--separate                  替换

2.3 退出码
----------------------------------

sed的退出码比较少，这里一一列举出来。

0
    成功
1
    无效命令
2
    一个海阔这多个输入文件不能被打开
3
    io错误
