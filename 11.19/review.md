d_model是总特征维度，num_heads是要并行的头数，因此每个head是64除以4

B T D如何变为B H T Dh：
先用view切分D，在view中设置4个头除以，于是得到B T H Dh
然后用transpose（1，2）换位得到 B H T Dh


合并过程，先用transpose（1，2) 将T H 替换过来，再用reshape（B T D）将H Dh压扁为一个维度

