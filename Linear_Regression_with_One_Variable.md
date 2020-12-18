# 二. 单个变量线性回归（Linear Regression with One Variable）
## 1. 模型和代价函数（Model and Cost funcion）  
   1.1 模型表达（Model Representation）  
   术语说明：  
   - x<sup>(i)</sup> 输入变量    
   - y<sup>(i)</sup> 输出变量  
   - (x<sup>(i)</sup>y<sup>(i)</sup>) 一对训练样本  
   - (x<sup>(i)</sup>y<sup>(i)</sup>);i=1,...,m 训练集  
监督学习是在给定训练集的条件下，学习函数h：X→Y，使得h（x）与相应的Y值，是一个“好”的预测器。这个函数h被称为假设函数。

<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/hypothesis.png'>
</p>

预测的目标变量是连续数值，比如房价，称为回归（regression）问题。预测的目标变量是有限个离散量，称为归类（classification）问题

## 2. 代价函数  
使用代价函数来**衡量**假设函数性能，通过计算假设函数输出量和实际输出的平均误差来进行评估。  
均方根形式的误差函数
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Cost%20Function.png'>
</p>

以线性回归为例，如何找到合适的 Theta_0和Theta_1，使得Cost Function最小化，是我们要解决的问题。
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Cost%20Function%20Example.png'>
</p>

## 3. 梯度下降  
改变变量Theta_0和Theta_1，寻找J(Theta_0，Theta_1)的最小值。  
比喻为下山，站在山上的某一点，逐步的往下走，直到找到局部的最小值点。  

<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Gradient%20Descent.png'>
</p>

<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Gradient%20Descent2.png'>
</p>

**以Theta_1为例子，不论初始值在什么位置，最终都可以收敛（与最小值的相对位置不同，斜率的正负也不同）**  
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Gradient%20Descent%20Slop.png'>
</p>

**下山的速率由学习速率参数Alpha决定。速率小意味着收敛速度慢，速率大有可能难以收敛。**
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/learning%20rate.png'>
</p>

**随着Theta值逐渐靠近最小点，斜率变小，步进也随之变小。**  
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/learning%20rate%20small%20step.png'>
</p>
** 梯度下降与求导数，导数为什么是下山最快方向，没有做过多的说明**

## 4. 梯度下降与线性回归  
**线性回归与梯度下降的结合**
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Gradient_descent_for_Linear_regression.png'>
</p>
**求偏导数，同时更新赋值**
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Gradient_descent_Algorithm.png'>
</p>

