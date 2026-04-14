# 仅面向Windows系统
>[!WARNING] 
>用户名、存放代码文件夹、数据集路径，**绝对不要出现中文** </font>

## 环境搭建
### 安装conda  
>教程链接：[知乎：https://zhuanlan.zhihu.com/p/510293011]
### conda换源（上海交大源）
打开终端（CMD 或 Anaconda Prompt），一次性复制下面的命令：  
```bash
conda config --add channels [https://mirrors.sjtu.edu.cn/anaconda/pkgs/free/](https://mirrors.sjtu.edu.cn/anaconda/pkgs/free/)
conda config --add channels [https://mirrors.sjtu.edu.cn/anaconda/pkgs/main/](https://mirrors.sjtu.edu.cn/anaconda/pkgs/main/)
conda config --add channels [https://mirrors.sjtu.edu.cn/anaconda/cloud/pytorch/](https://mirrors.sjtu.edu.cn/anaconda/cloud/pytorch/)
conda config --set show_channel_urls yes  
```

### pip换源（阿里云源）
90% 的第三方包需要pip安装，继续在终端输入这行命令，将全局 pip 源设为阿里云：  
```bash
pip config set global.index-url [https://mirrors.aliyun.com/pypi/simple/](https://mirrors.aliyun.com/pypi/simple/)
```
### 开辟独立环境
为你的项目新建一个纯净的环境(以后每次跑代码前，先激活对应的环境)
```bash
 conda create -n phm_env(环境名) python=3.9
 conda activate phm_env
```
---
## CUDA与pytorch
### 查看电脑显卡的上限
在终端中输入
```bash
nvidia-smi
```
表格右上角的 `CUDA Version: XX.X`。这个数字代表你显卡支持的**最高** CUDA 版本。
### 安装PyTorch（现在安装GPU版Torch貌似不需要手动安装CUDA）
>参考链接[知乎：https://zhuanlan.zhihu.com/p/694533401]
### 如需完整环境
>安装完整版 CUDA Toolkit 和 cuDNN  
>参考链接[【保姆级】Windows 安装 CUDA 和 cuDNN:https://zhuanlan.zhihu.com/p/32400431090]
### 终极验证


