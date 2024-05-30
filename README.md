# final1
训练SimCLR模型
准备数据集:
CIFAR-100 数据集的加载和预处理，包括数据增强（SimCLRDataTransform）。
定义模型和优化器:
使用 ResNet18 作为基础模型，定义 SimCLR 模型和 Adam 优化器。
训练过程:
训练200个epoch，使用NT-Xent对比损失函数。每个epoch结束后记录训练损失。
线性分类器训练
冻结预训练好的SimCLR模型的特征提取器。
定义线性分类器:
一个线性层用于从冻结的特征中进行分类。
训练过程:
使用CIFAR-100训练集进行训练200个epoch，记录训练损失和准确率。
测试过程:
使用CIFAR-100测试集进行测试，计算测试准确率
超参数修改
修改训练SimCLR模型:
num_epochs: 训练的epoch数量。
temperature: 对比损失中的温度参数。
batch_size: 数据加载器中的批量大小。
learning_rate: 优化器的学习率。
train_simclr(num_epochs=100, temperature=0.7, batch_size=512, learning_rate=0.0005)
训练线性分类器:
num_epochs: 训练的epoch数量。
learning_rate: 优化器的学习率。
train_linear_classifier(num_epochs=150, learning_rate=0.0001)
