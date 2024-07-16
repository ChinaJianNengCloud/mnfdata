# 项目概述
该项目是分类任务，由于数据集的性质，采用度量学习的方式来进行训练分类。
原项目路径:https://kevinmusgrave.github.io/pytorch-metric-learning/inference_models/
参考项目路径:https://github.com/xxcheng0708/pytorch-metric-learning-template/tree/main/utils

# 数据介绍
数据格式是xlsx，有4个表，分别是训练集，留出集，西溪验证集，浙一验证集
每个表的列数相同，其中第一列为类别(因变量)，其余类为自变量
其中训练集有318条数据，留出集有45条数据，西溪验证集有49条数据，浙一验证集有52条数据

# 实验介绍
目前做了1组实验
## 实验1
模型架构，trunk是MLP，embedding是MLP，classifier是MLP
其中trunk输入是32(不算batchsize)，隐藏层有3层，分别是64，64，64，输出是32
其中embedding输入是32，输出是64
其中classifier输入是64，输出是2


##实验2
模型架构，trunk是one CONV，embedding是MLP，classifier是MLP
其中trunk输入是1*32的一维向量(不算batchsize)，有三层，第一层16次卷积，第二层32次卷积，第三层1次卷积，输出是1*32
其中embedding输入是32，输出是64
其中classifier输入是64，输出是2