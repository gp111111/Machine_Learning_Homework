# Machine_Learning_Homework
Andrew Ng的机器学习的课，用Python实现(粗略版)  
边学边记录 
# 进行机器学习的算法
[holehouse写的笔记，很强，学习](http://www.holehouse.org/mlclass/?spm=a2c6h.12873639.0.0.64b13873e0Es3k)
## 线性回归
线性回归可以处理regression问题，对regression来说是一些连续的值，比较好的例子就是：房价预测  
### 一元线性回归/多元线性回归  
本质是差不多的，不同的是features，另外有很多细节
### 梯度下降/正规方程
这两个求解能让Cost function最小的theta（参数），在我的理解就是，这些只是算法的解决办法，也就是说，比算法要低一级
## 逻辑回归
线性回归不再好解决这类分类问题Classification，也就是分离的值
### 两类或多类逻辑回归
而且因为要输出的一般表示为1的可能性，线性回归计算出的数也不会保证在0～1之间，所以就利用sigmoid 函数和"线性方程"(广义一点)来实现。Cost function和Penalty function的形式也有变化，但是对于gradient形式和theta更新的形式还和之前相同（求偏微分）  
对多类来讲，每次挑两类，最后取计算概率最大的那一类
### 利用scipy的opt来进行训练
这一章没有像上一章一样寻求梯度下降，自己写，而是用了scipy里的optimal来进行求解更加方便
### regularization正则化处理
这个防止过拟合出现，增加了一个lambda值
