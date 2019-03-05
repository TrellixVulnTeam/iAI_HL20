# AI Play on Ubuntu Platform

AI实验环境搭建和深度学习算法安装实验     
      
**安装环境**  
*其他环境类似* 
```
硬件环境: CPU i7 / NVIDIA TITAN V / SSD
系统环境：Ubuntu 16.04 64bit
安装软件：CUDA9.0 / caffe / YOLO V3 / Protobuf / Matlab / VIM
````
---
### 目录
1. [AI基础环境搭建和设置](src/ai_base_env.md#ai基础环境搭建和设置)
   1. [安装Ubuntu和Windows双系统](src/ai_base_env.md#安装ubuntu和windows双系统)   
   2. [安装NVIDIA驱动](src/ai_base_env.md#安装nvidia驱动)   
       - [安装NVIDIA驱动所需的依赖包](src/ai_base_env.md#安装nvidia驱动所需的依赖包)   
       - [禁用Ubuntu自带的显卡驱动](src/ai_base_env.md#禁用ubuntu自带的显卡驱动)   
       - [安装NVIDIA官方显卡驱动](src/ai_base_env.md#安装nvidia官方显卡驱动)   
       - [配置NVIDIA环境变量](src/ai_base_env.md#配置环境变量)   
       - [查看NVIDIA显卡驱动版本](src/ai_base_env.md#查看NVIDIA驱动版本)    
   3. [安装CUDA](src/ai_base_env.md#安装cuda)   
       - [安装CUDA步骤](src/ai_base_env.md#安装cuda步骤)    
       - [修改配置文件](src/ai_base_env.md#修改配置文件)    
       - [查看CUDA版本](src/ai_base_env.md#查看cuda版本)
       - [卸载CUDA的方法](src/ai_base_env.md#卸载cuda的方法)    
   4. [安装cuDNN](src/ai_base_env.md#安装cudnn)    
   5. [安装Anaconda](src/ai_base_env.md#安装anaconda)    
   6. [安装OpenCV](src/ai_base_env.md#安装opencv)   
       - [下载OpenCV](src/ai_base_env.md#下载opencv)
       - [编译OpenCV](src/ai_base_env.md#编译opencv)
       - [安装OpenCV](src/ai_base_env.md#安装opencv)
       - [卸载OpenCV](src/ai_base_env.md#卸载opencv)
   7. [TensorRT](src/ai_base_env.md#tensorrt) 
       - [安装TensorRT](src/ai_base_env.md#安装tensorrt)    
         - [TensorRT环境变量设置](src/ai_base_env.md#tensorrt1)
         - [安装Python的TensorRT包](src/ai_base_env.md#tensorrt2)
         - [安装uff](src/ai_base_env.md#tensorrt3)
         - [验证TensorRT是否安装成功](src/ai_base_env.md#tensorrt4)
         - [TensorRT安装过程中遇到的问题以及解决方法](src/ai_base_env.md#tensorrt5)
       - [TensorRT生成Engine](src/ai_base_env.md#tensorrt生成engine)
         - [TensorRT Caffe Engine](./src/tensorrt/tensorrt-4.0.1.6/caffe_to_tensorrt.ipynb)
         - [TensorRT Tensorflow Engine](./src/tensorrt/tensorrt-4.0.1.6/tf_to_tensorrt.ipynb)
         - [Manually Construct Tensorrt Engine](./src/tensorrt/tensorrt-4.0.1.6/manually_construct_tensorrt_engine.ipynb)
   8. [安装Caffe](src/ai_base_env.md#安装caffe)   
       - [Python2下安装Caffe](src/ai_base_env.md#python2下安装cafe) 
       - [Python3下安装Caffe](src/ai_base_env.md#python3下安装cafe )
   9.  [安装YOLO V3](src/ai_base_env.md#安装yolov3)
   10. [安装Protobuf](src/ai_base_env.md#安装protobuf)
   11. [Linux MATLAB 2018a 安装教程及启动失败解决办法](src/ai_base_env.md#安装matlab)

2.  [深度学习算法安装和环境设置](./src/algorithm_install.md)
     - [监视GPU和CPU资源利用情况](./src/algorithm_install.md#监视gpu和cpu资源利用情况)
     - [Python项目requirements.txt的生成和使用](./src/algorithm_install.md#python项目requirements.txt的生成和使用)
     - [Anaconda环境下TensorFlow和Pytorch共存问题](./src/algorithm_install.md#anaconda环境下tensorflow和pytorch共存问题)
     - [深度学习服务器FAQ](./src/ai_server_FAQ.md#深度学习服务器faq)
       - [docker常用命令](./src/ai_server_FAQ.md#docker常用命令) 
       - [多显卡训练问题](./src/ai_server_FAQ.md#多显卡训练问题) 
       - [远程访问服务器Jupyter Notebook](./src/ai_server_FAQ.md#远程访问服务器jupyter-notebook)
         - [方法1 ssh远程使用jupyter notebook](./src/ai_server_FAQ.md#方法1-ssh远程使用jupyter-notebook)
         - [方法2 利用jupyter notebook自带的远程访问功能](./src/ai_server_FAQ.md#方法2-利用jupyter-notebook自带的远程访问功能)
     - [Shadowsocks 安装](./src/ss.md#shadowsocks安装)
       - [Shadowsocks说明](./src/ss.md#shadowsocks说明)
       - [安装Shadowsocks-qt5](./src/ss.md#安装shadowsocks-qt5)
       - [安装electron-ssr](./src/ss.md#安装electron-ssr)
       - [配置Chrome浏览器](./src/ss.md#配置chrome浏览器)
     - [Faster R-CNN编译问题](./src/algorithm_install.md#faster-r-cnn编译问题)

3.  [Ubuntu FAQ](./src/linux_env_set.md#ubuntu-faq)
     - [Docker安装与使用](./src/linux_env_set.md#docker安装与使用)
       - [Docker安装](./src/linux_env_set.md#docker安装)
       - [Docker使用](./src/linux_env_set.md#docker使用)
     - [Linuxbrew安装](./src/linux_env_set.md#linuxbrew安装)
       - [安装linuxbrew](./src/linux_env_set.md#安装linuxbrew)
       - [linuxbrew必装包](./src/linux_env_set.md#linuxbrew必装包)
       - [brew常用命令](./src/linux_env_set.md#brew常用命令)
       - [linuxbrew注意事项](./src/linux_env_set.md#linuxbrew注意事项)
     - [Ubuntu每次开机后提示检测到系统程序出现问题的解决方法](./src/linux_env_set.md#ubuntu每次开机后提示检测到系统程序出现问题的解决方法)
     - [Ubuntu循环登陆问题](./src/linux_env_set.md#ubuntu循环登陆问题)
     - [安装Python依赖库](./src/linux_env_set.md#安装python依赖库)
     - [安装Chrome浏览器](./src/linux_env_set.md#安装chrome浏览器)
     - [pip/pip3安装报错问题](./src/linux_env_set.md#pip和pip3安装报错)
     - [关于Ubuntu 16.04LTS下安装Spyder3的问题](./src/linux_env_set.md#ubuntu-16下安装spyder3)
     - [安装搜狗输入法](./src/linux_env_set.md#安装搜狗输入法)
     - [WPS无法输入中文](./src/linux_env_set.md#wps无法输入中文)
     - [安装赛睿霜冻之蓝V2驱动](./src/linux_env_set.md#安装赛睿霜冻之蓝v2驱动)
     - [zsh oh-my-zsh默认shell的最佳替代品](./src/linux_env_set.md#zsh-oh-my-zsh默认shell的最佳替代品)
       - [查看系统shell环境](./src/linux_env_set.md#查看系统shell环境)
       - [安装zsh](./src/linux_env_set.md#安装zsh)
       - [安装vimrc](./src/linux_env_set.md#安装vimrc)
       - [安装oh-my-zsh](./src/linux_env_set.md#安装oh-my-zsh)
       - [安装zsh-syntax-highlighting](./src/linux_env_set.md#安装zsh-syntax-highlighting)
       - [安装colorls](./src/linux_env_set.md#安装colorls)
     - [vim配置](./src/linux_env_set.md#vim配置)
       - [YouCompleteMe实现vim自动补全](./src/linux_env_set.md#youcompleteme实现vim自动补全)
       - [vim最终配置](./src/linux_env_set.md#vim最终配置)
     - [Tmux配置与使用](./src/linux_env_set.md#tmux配置与使用)
       - [Tmux配置](./src/linux_env_set.md#tmux配置)
       - [Tmux使用手册](./src/linux_env_set.md#tmux使用手册)
     - [Sublime Text 3配置问题](./src/linux_env_set.md#sublime-text-3配置问题)
     - [Visual Studio Code配置问题](./src/linux_env_set.md#visual-studio-code配置问题)    
     - [Ubuntu查看和关闭进程](./src/linux_env_set.md#ubuntu查看和关闭进程)
     - [Ubuntu后台执行命令](./src/linux_env_set.md#ubuntu后台执行命令)   
     - [查看系统状态](./src/linux_env_set.md#查看系统状态)

4.  [参考资料](#参考资料)


---
##  参考资料  
> 1. [win10下安装Ubuntu16.04双系统](https://blog.csdn.net/s717597589/article/details/79117112/)
> 2. [Ubuntu 16.04+CUDA 9.1+cuDNN v7+OpenCV 3.4.0+Caffe+PyCharm 完全安装指南](https://blog.csdn.net/balixiaxuetian/article/details/79154013)
> 3. [Install caffe with anaconda(3.6) on ubuntu16.04](http://www.yaoingwen.com/ubuntu16-04-anaconda-3-6-caffe/)
> 4. [caffe编译遇到的问题](https://blog.csdn.net/m0_37407756/article/details/70789271)
> 5. [Linux MATLAB 2018a 安装教程及启动失败解决办法](https://blog.csdn.net/ouening/article/details/79751393)
> 6. [关于Ubuntu16.04LTS下Python版本和安装Spyder3的问题？](https://www.zhihu.com/question/51248022/answer/142596984)
> 7. [zsh + oh-my-zsh 默认shell的最佳替代品](https://blog.phpgao.com/oh-my-zsh.html)
> 8. [Terminal Experience](https://medium.com/@caulfieldOwen/youre-missing-out-on-a-better-mac-terminal-experience-d73647abf6d7)
> 9. [远程访问服务器Jupyter Notebook的方法](https://www.jianshu.com/p/8fc3cd032d3c)    
> 10. [Jupyer Notebook官方指南](https://jupyter-notebook.readthedocs.io/en/latest/public_server.html#notebook-server-security)
> 11. [设置 jupyter notebook 可远程访问](https://blog.csdn.net/simple_the_best/article/details/77005400)
> 12. [Docker — 从入门到实践](https://github.com/yeasy/docker_practice)
> 13. [Docker 官方 Ubuntu 安装文档](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
> 14. [.tmux配置](https://github.com/gpakosz/.tmux)
> 15. [Tmux 快捷键 & 速查表](https://gist.github.com/ryerh/14b7c24dfd623ef8edc7)
