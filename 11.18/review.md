为什么 Mask 必须在 Softmax 之前 应用？
在于 Softmax 的数学特性和概率归一化,在其之前应用mask会让mask总和仍然为1，即重新归一化


为什么 Padding Mask 只屏蔽 Key，不自动把 Padding Query 的输出置零？
Padding Key：表示“这个位置是没有意义的 pad 词，而Padding Query：表示“当前位置本身是 pad，不需要产出有意义的特征”。