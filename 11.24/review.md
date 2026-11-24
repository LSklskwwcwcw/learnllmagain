Categorical(logits=...):构建一个离散概率分布。接收网络输出的未归一化分数 logits，在内部自动用 Softmax 转换成概率

.sample():按概率随机抽样一个动作。如果分布是 [0.73, 0.27]，它有 73% 的概率选动作 0，27% 的概率选动作 1。


.log_prob(action):计算刚才抽出的那个动作的对数概率

-(log_prob * reward).mean():计算 REINFORCE 的 Loss。

为什么奖励（reward）不需要可微？
因为环境（Environment）是一个“黑盒”，无法对其进行求导，也不应该对其求导。