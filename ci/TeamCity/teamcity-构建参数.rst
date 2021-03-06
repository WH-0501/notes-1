teamcity 构建参数
=================

teamcity-web-parameters
-----------------------

从web服务填充可选动态参数

`GitHub
teamcity-web-parameters <https://github.com/grundic/teamcity-web-parameters>`__

动态构建参数
------------

.. figure:: http://oi480zo5x.bkt.clouddn.com/teamcity-02-parameter.png
   :alt: teamcity-02-parameter

   teamcity-02-parameter

.. figure:: http://oi480zo5x.bkt.clouddn.com/teamcity-03-parameter-02.png
   :alt: teamcity-03-parameter-02

   teamcity-03-parameter-02

保存

.. figure:: http://oi480zo5x.bkt.clouddn.com/teamcity-04-parameter-03.png
   :alt: teamcity-04-parameter-03

   teamcity-04-parameter-03

只需要在后面的构建过程中引用 **select** 参数就行

teamcity从命令行设置构建参数
----------------------------

To set build parameters from command line you need to use the following
commands:

Build Step #1:

.. code:: shell

    #!/bin/bash
    echo "##teamcity[setParameter name='env.ddd' value='fff']"
    echo "##teamcity[setParameter name='env.datetime' value='$(date)']"

The values of initialized parameters will be avaliable on the next build
step:

Build Step #2:

.. code:: shell

    #!/bin/bash
    echo $ddd
    echo $datetime

使用web提供动态参数
-------------------

有时间补充
