# pytorch和pytorch_geometric的安装

在安装好了anaconda之后安装pytorch变得很简单了

## Pytorch

首先创建环境

```
conda create -n pytorch_geometric python=3.8
```

然后去pytorch官网找命令行:

![image-20220327113430552](https://picture-of-notebook.oss-cn-hangzhou.aliyuncs.com/img/image-20220327113430552.png)

这边建议把VPN给关掉，开了VPN好像会出问题，这一步最好用conda安装，用pip好像也容易出问题。有英伟达GPU安装stable和cuda的11.3的

```shell
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
```

没有GPU的安装CPU版本：

```shell
conda install pytorch torchvision torchaudio cpuonly -c pytorch
```

## Pytorch Geometric

安装好pytorch之后，就可以安装pytorch_geometric

可以采用conda和pip的两种模式，conda方式更为方便，但是两种模式都能成功

Cuda的CPU/GPU版本：

```
conda install pyg -c pyg
```

pip的GPU版本

```shell
pip install torch-scatter -f https://data.pyg.org/whl/torch-1.11.0+cu113.html
pip install torch-sparse -f https://data.pyg.org/whl/torch-1.11.0+cu113.html
pip install torch-cluster -f https://data.pyg.org/whl/torch-1.11.0+cu113.html
pip install torch-spline-conv -f https://data.pyg.org/whl/torch-1.11.0+cu113.html
pip install torch-geometric
```

pip的CPU版本:

```
pip install torch-scatter==latest+cpu -f https://pytorch-geometric.com/whl/torch-1.5.0.html

pip install torch-sparse==latest+cpu -f https://pytorch-geometric.com/whl/torch-1.5.0.html

pip install torch-cluster==latest+cpu -f https://pytorch-geometric.com/whl/torch-1.5.0.html

pip install torch-spline-conv==latest+cpu -f https://pytorch-geometric.com/whl/torch-1.5.0.html

pip install torch-geometric
```

