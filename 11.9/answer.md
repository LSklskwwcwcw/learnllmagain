tensor 是张量，是ai的基础运算单元
loss是损失，gradient是梯度，我理解二者的区别是，首先，loss是需要被计算来评估当前处于梯度的什么环节，最终优化的目标是梯度下降至最优
backward是反向传播，负责将这轮的调整参数需求反向传播至前向传播处，令其之后按指标优化
optimizer.step是优化器，我忘记了具体的内容，我记得可能是根据loss的结果来做优化调整



纠正：
Loss：衡量预测结果与目标之间有多大差距。
Gradient：告诉我们改变参数时，Loss 如何变化。
Optimizer：利用梯度决定怎样更新参数。

参数 → Forward → Loss
Backward → Gradient
Optimizer.step() → 更新参数
下一次 Forward