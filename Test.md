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


-tx-
|分布类型|概率密度函数|期望$E(X)$|$方差D(X)$|
|:---:|:---:|:---:|:---:|
|两点分布|$$P\left \{ X=0 \right \}=1-p,P\left \{ X=1 \right \}=p$$|$$p$$|$$p(1-p)$$|
|泊松分布|$$P\left \{ X=k \right \}=\frac{\lambda ^k}{k!}e^{-\lambda} ,k=0,1,2,\cdots $$|$$\lambda$$|$$\lambda$$|
|二项分布|$$P\left \{ X=k \right \}=C_{n}^{k}\cdot p^k \cdot (1-p)^{n-k},k=0,1,2,\cdots n$$|$$np$$|$$np(1-p)$$|
|均匀分布|$$f(x)=\left\{\begin{matrix}\displaystyle {\frac{1}{b-a}}, & a<x<b\\0,& else\end{matrix}\right.$$|$$\frac{a+b}{2}$$|$$\frac{(b-a)^2}{12}$$|
|指数分布|$$f(x)=\left\{\begin{matrix}\lambda e^{-\lambda x}, &x>0 \\0 & else\end{matrix}\right.$$|$$\frac{1}{\lambda}$$|$$\frac{1}{\lambda^2}$$|
|正态分布|$$\displaystyle {f(x)=\frac{1}{\sqrt[]{2 \pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}},-\infty <x<\infty $$|$$\mu$$|$$\sigma^2$$|