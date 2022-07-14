该项目实现AlexNet，VGGNet，GoogleNet，BN-Inception/Inceptionv2，Inceptionv3，ResNet，Inceptionv4，ResNeXT，DenseNet，SENet十种经典模型。

**主要参考代码**：https://github.com/weiaicunzai/pytorch-cifar100

**开发环境**：Python 3.8.3 ；Pytorch 1.7.1+cu110；PyCharm 2019。

**项目结构**：

- 目录models：包括AlexNet，VGGNet，GoogleNet，BN-Inception/Inceptionv2，Inceptionv3，ResNet，Inceptionv4，ResNeXT，DenseNet，SENet十种经典模型的实现。
- 文件dataset：是数据类，定义数据类型。
- 文件train：完成训练。
- 文件utils：是一些工具类函数。

每次可以通过设置命令行参数运行train.py文件，训练不同的模型。使用交叉熵损失函数，小批量梯度下降，Adam优化器，采用一轮的学习率warm up。因为显存限制，设置不同的批量大小和学习率，具体设置与运行结果如下所示。

|                          | Batch-size | Learning  rate | Accuracy |
| :----------------------: | ---------- | -------------- | -------- |
|         AlexNet          | 256        | 0.001          | 31.01%   |
|          VGGNet          | 256        | 0.0001         | 28.09%   |
|        GoogleNet         | 128        | 0.001          | 42.36%   |
| BN-Inception/Inceptionv2 | 32         | 0.0015         | 38.21%   |
|       Inceptionv3        | 32         | 0.001          | 34.16%   |
|          ResNet          | 32         | 0.001          | 27.76%   |
|       Inceptionv4        | 16         | 0.001          | 21.09%   |
|         ResNeXT          | 64         | 0.001          | 40.59%   |
|         DenseNet         | 64         | 0.001          | 45.75%   |
|          SENet           | 64         | 0.001          | 39.49%   |



