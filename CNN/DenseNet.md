# Densely Connected Convolutional Networks
## Abstract

## Architecture
### Dense Block
下图是Dense Block的架构图。在传统的CNN中，如果有L层则有L个连接。而在DenseNet（密集连接卷积网络）中，L层网络有L\*(L+1)/2个连接。<br>
与ResNet（残差网络）不同的是，DenseNet不是在传递给某一层的特征相加（combine），而是进行拼接（concatenate）<br>
FFNN：xl = Hl(xl-1)    （直接经过非线性函数输出）<br>
ResNet：xl= Hl(xl−1) + xl−1   （）<br>
DenseNet：<br>
x0为输入的图像，xl为第l层的输出，L为网络的层数，第l层网络有一个非线性函数Hl(\*)，其中Hl(\*)是一个混合操作函数，图中包含3个组件（BN、ReLU、Conv），当然这个在后面的架构中还会增加其他组件。


![](https://github.com/tangshisong/deep-learning/blob/master/image/1.png)
![](https://github.com/tangshisong/deep-learning/blob/master/image/2.png)
