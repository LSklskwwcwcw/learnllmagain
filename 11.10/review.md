requires_grad=True 的作用是给变量追加梯度追踪，也就是说，这个变量被定义为需要梯度的，也就是说需要通过梯度来对这个变量追加更新

backward() 与 optimizer.step() 有什么区别：

backward根据gradient提供的梯度来看怎么参数发生了怎样的改变
而optimiezer则决定怎么更新改变参数

为什么 .grad 会累积？怎样清零：
grad通过反向传播累积，待到一次参数更新后就归零