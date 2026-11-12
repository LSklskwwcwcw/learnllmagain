optimizer.zero_grad():遍历所有require_grad的参数，比如w和b，将他们的.grad清零


loss.backward():触发反向传播，利用链式法则，将每个参数这轮的梯度计算出来然后塞进对应参数的.grad中

step则是根据当前的优化器，读取每个参数上的.grad，去真正修改参数的值



如果两个不同的优化器使用的参数不同，不具备参考价值
