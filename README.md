# Bilibili粉丝牌助手  
## 介绍  
这个库增加了对其他推送方式的支持，依赖[onepush](https://github.com/y1ndan/onepush)  
- [OnePush使用指南](https://github.com/Huli-fox/bili-live-heart/blob/dev/docs/Guide/OnePush.md)  
  
## 开始使用  
> 开始使用前，请确保您已经安装了Python运行环境（不低于3.7），并且已经理解[OnePush使用指南](https://github.com/Huli-fox/bili-live-heart/blob/dev/docs/Guide/OnePush.md)。  

- ### 本地部署  
  > 运行环境Windows10，Python3.7.9  
  
  #### 1.下载程序  
  到[这里](https://github.com/Huli-fox/bili-live-heart/releases/)下载最新版本的Source code (zip)，并解压至不含中文的路径  
  此处以1.2.1-EX版本为例  
  ![1.png](https://s2.loli.net/2022/04/26/QYdJD4Ox9TaENRV.png)  
  #### 2.创建虚拟环境 （如果您对版本隔离没有需求，请跳过本步骤）  
  打开程序根目录，按住shift鼠标右击，选择在此处打开命令窗口，依次输入以下内容并回车执行：  
  > python -m venv venv  
  cd venv/Scripts  
  activate.bat  
  
  ![2.png](https://s2.loli.net/2022/04/26/MTcb89A3SEWfmqF.png)  
  ![3.png](https://s2.loli.net/2022/04/26/DO93gFd2vaXcb7s.png)  
  最后一条命令执行完应该是这样（注意别急着把窗口关了，下面都要用）  
  ![4.png](https://s2.loli.net/2022/04/26/wzNXhAgQFKYk8UP.png)  
  #### 3.安装依赖库  
  命令行切换路径到程序根目录，输入以下命令并回车执行：  
  > pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple  
  
  使用虚拟环境的接着第二步打开的命令行窗口执行以下命令：  
  > pip install -r ../../requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple  
  
  出现Successfully即为成功  
  ![5.png](https://s2.loli.net/2022/04/26/FoHzl24ck9S5Vx1.png)  
  #### 4 .配置用户信息  
  打开user.toml（打不开就用记事本打开）  
  配置方法见[原版文档](https://xiaomiku01.github.io/bili-live-heart/LocalDocker/#_1-3-%E9%85%8D%E7%BD%AE%E7%94%A8%E6%88%B7%E4%BF%A1%E6%81%AF)，最后一行onepush参数配置见[OnePush使用指南](https://github.com/Huli-fox/bili-live-heart/blob/dev/docs/Guide/OnePush.md)  
  #### 5.运行  
  命令行输入以下命令并回车执行：  
  > python index.py  
  
  虚拟环境：  
  > cd ../../  
  python index.py  
  
- ### 云函数部署  
  见[原版文档](https://xiaomiku01.github.io/bili-live-heart/TencentCloud/)，把环境变量sendkey改成onepush，然后按照[这个](https://github.com/Huli-fox/bili-live-heart/blob/dev/docs/Guide/OnePush.md)配置就好了  
  注意下onepush环境变量是**必填**的，要不然云函数报错  
  
- ### Docker  
  见原版文档，[配置用户信息](https://xiaomiku01.github.io/bili-live-heart/LocalDocker/#_2-2-%E9%85%8D%E7%BD%AE%E7%94%A8%E6%88%B7%E4%BF%A1%E6%81%AF)时：  
  > SERVER_CHAN_SENDKEY=""  
  
  改成  
  > ONEPUSH=""  
  
  就行了（大概），如果报错把双引号改成单引号试试（没用过Docker，相关问题无法回答，见谅）
  
## 附言  
**5.11**  
不知道说什么好  
遗憾的、讽刺的、现实的  
不出意外的话这应该是这个库最后一次更新  
**5.2**  
增加了Docker支持，不保证能正常运行  
**4.30**  
修正了文档中的一个错误  
能力有限，问题可能没法都解决，多见谅（  
**4.26**  
写了个教程，如果有问题欢迎提issue  
**4.23**  
腾讯云函数不给白嫖了，建议早点迁移  
如图  
![pic2.png](https://s2.loli.net/2022/04/23/sE72xQ9o6U8pr1b.png)  
![pic1.png](https://s2.loli.net/2022/04/23/4DyzlrcWnsS63p1.png)  
