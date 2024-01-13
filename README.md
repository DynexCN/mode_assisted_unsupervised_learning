# 受限玻尔兹曼机的模式辅助无监督学习
受限玻尔兹曼机（RBMs）是一类强大的生成模型，但它们的训练需要计算一个梯度，与典型的有监督反向传播和典型损失函数不同，这个梯度甚至在近似上也是极其困难的。在这里，我们展示了将标准梯度更新与RBMs基态（模式）样本构造的梯度方向适当结合，相比传统梯度方法，显著改善了训练效果。我们称之为“模式辅助训练”的这种方法，促进了更快的训练和稳定性，除了更低的收敛相对熵（KL散度）。我们在可以精确计算KL散度的合成数据集上以及更大的机器学习标准数据集（MNIST）上展示了其有效性。所提出的模式辅助训练可以与任何给定的梯度方法结合使用，并且可以轻松扩展到更一般的基于能量的神经网络结构，例如深度、卷积和无限制的玻尔兹曼机。

以下图表显示了模式辅助训练与CD-1的优越性：

![OUTOUT](https://github.com/DynexCN/mode_assisted_unsupervised_learning/blob/main/output.png)

# 作为基于Python类的模式辅助QRBM（基于PyTorch）

可以通用使用。以下是使用MNIST数据集的示例，对比CD-1和模式辅助。在传统模型训练（CD）在某一点无法改进的情况下（蓝线），新的基于PyTorch的模式辅助量子玻尔兹曼机（QRBM）突破了这一界限，证明在模式再现和细节方面具有卓越能力。

要运行代码：

```
python3 main.py
```


![Figure_8](https://github.com/DynexCN/mode_assisted_unsupervised_learning/blob/main/Figure_8.png)

![Figure_1](https://github.com/DynexCN/mode_assisted_unsupervised_learning/blob/main/Figure_1.png)

### 参考文献
[Mode-assisted unsupervised learning of restricted Boltzmann machines](https://arxiv.org/pdf/2001.05559.pdf), Communications Physics volume 3, Article number:105 (2020)
