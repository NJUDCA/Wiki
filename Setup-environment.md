# Setup environment for NLP models on WinOS

Use Anaconda to setup an virtula env
1. Install Anaconda3
默认添加路径到环境变量，安装成功后有：
Anaconda Navigator，提供图形界面操作，管理环境和包；
Anaconda Prompt，提供命令行操作，管理环境和包，还可执行脚本；

2. Create new env
```bash
conda create -n <env_name> python=3.5
```

3. Activate and install packages
推荐通过conda安装，这样出错的概率小；
如果conda源未提供相应的包，则通过pip安装
```bash
soruce activate <env_name>
conda install tensorflow, numpy
```

4. Use the virtual env as python project interpreter