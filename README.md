# d2l-

d2l深度学习框架搭建https://zh.d2l.ai/；

MXNet的GPU版本；PyTorch的GPU版本；TensorFlow的GPU版本；PaddlePaddle的GPU版本。

硬件基于笔记本联想y7000p，GTX1060，运存三星8GB DDR4 2666；硬盘三星SSD 512GB。

软件基于Windows10；miniconda3；Python3.8；CUDA10.1。


一.创建工作区：
conda create --name d2l python=3.8 -y
conda activate d2l
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/

我们的下一步是安装d2l包，以方便调取本书中经常使用的函数和类：
conda install -c conda-forge d2l==0.17.6

删除环境：
conda deactivate
conda env list
conda env remove -n d2l

以下是隔离环境框架（适配性更好，不会产生依赖冲突）

二.安装深度学习框架
✅1.MXNet的GPU版本
conda create --name d2lMXNet python=3.8 -y
conda activate d2lMXNet
pip install d2l==0.17.6 -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.tuna.tsinghua.edu.cn
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda install numpy=1.16.6 -c conda-forge -y
pip install mxnet-cu101==1.7.0 -f https://dist.mxnet.io/python

✅2.PyTorch的GPU版本
conda create --name d2lPyTorch python=3.8 -y
conda activate d2lPyTorch
pip install d2l==0.17.6 -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.tuna.tsinghua.edu.cn
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda install numpy=1.16.6 -c conda-forge -y
pip install torch==1.12.0 torchvision==0.13.0 -i https://pypi.tuna.tsinghua.edu.cn/simple

✅3.TensorFlow的GPU版本
conda create --name d2lTensorFlow python=3.8 -y
conda activate d2lTensorFlow
pip install d2l==0.17.6 -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.tuna.tsinghua.edu.cn
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
pip install tensorflow-gpu==2.3.0 -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install tensorflow-probability==0.11.0 -i https://pypi.tuna.tsinghua.edu.cn/simple

✅4.PaddlePaddle的GPU版本
conda create --name d2lPaddlePaddle python=3.8 -y
conda activate d2lPaddlePaddle
pip install d2l==0.17.6 -i https://pypi.tuna.tsinghua.edu.cn/simple --trusted-host pypi.tuna.tsinghua.edu.cn
python -m pip install paddlepaddle==2.4.2 -i https://pypi.tuna.tsinghua.edu.cn/simple
