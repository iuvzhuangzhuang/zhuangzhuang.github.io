---
layout:     post
title:      Virtualenvwrapper
subtitle:   python虚拟环境详情
date:       2020-05-28
author:     Twenty-Nine
header-img: img/Virtualenv.jpg
catalog: 	 true
tags:
    - python
    - 虚拟环境
---

# virtualenvwrapper

***python虚拟环境安装及使用***

## 安装Virtualenvwrapper

- Linux安装
  - pip install virtualenvwrapper
- windows安装
  - pip install virtualenvwrapper-win

## virtualenvwrapper基本使用

1. 创建虚拟环境

   ```
   mkvirtualenvwrapper my_env
   ```

   *会在当前登录的用户文件夹下创建一个名为Envs目录，然后将创建的虚拟环境安装到目录下，以后所有的虚拟环境都会在这里安装*

   ![VirtualenvWrapper](https://s1.ax1x.com/2020/05/28/teVGjI.png)

2. 切换环境

   ```
   workon my_env
   ```

   work意思是工作，on意思是在什么上，命令意思就是在哪个环境上工作，方便记忆命令

3. 退出当前环境

   ```
   deactivate
   ```

4. 删除环境

   ```
   rmvirtualenv xxx-env
   ```

   删除命令特别像Linux的删除命令

5. 呈现所有的虚拟环境

   ```
   lsvirtualenv 
   ```

6. 快速进入虚拟环境所在目录

   ```
   cdvirtualenv xxx_env
   ```



## 修改Virtualenv 的默认路径

Virtualenvwrapper初始Envs文件会创建在当前登录用户的子目录下，由于后期开发需要安装很多第三方软件包，虚拟环境装在C盘中，占用内存比较庞大。

在我的电脑-->右键属性-->高级系统设置-->环境变量-->系统变量-->新建名字为WORK_HOME 路径为你想要存放的地址路径

这样，你创建的虚拟环境地址就改为你需要他存在的地址了

创建一个环境进行检测

```
mkvirtualenv xxx-env
```

使用快速进入环境目录查看路径是否更改成功

```
cdvirtualenv xxx-env
```

## 创建环境时指定python版本

指定python版本

```
mkvirtualenv --python==python解释器路径 python_env
```

使用--python指定你需要创建的虚拟环境的python版本，路径为你的python解释器路径 python_env是环境名称，可以自行更改







