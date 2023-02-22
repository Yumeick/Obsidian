$$\sqrt{x}$$
```python
# 引入随机变量X
X=[0, 1]    #在当前车站有无人下车？
station= 10 #车站数量
passenger= 20   #旅客数量
p= 1 / station  #一位旅客在任一车站下车的概率
EX=0

for i in range(station):
    p_0= (1-p)**passenger
    EX_0= X[0] * p_0
    EX_1= X[1] * (1-p_0)
    EX+= (EX_0+EX_1)
print("E(X)={:.3f}".format(EX))
```

