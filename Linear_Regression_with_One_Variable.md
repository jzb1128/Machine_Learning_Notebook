# 二. 单个变量线性回归（Linear Regression with One Variable）
1. 模型和代价函数（Model and Cost funcion）  
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

2. 代价函数
通过计算假设函数输出量和实际输出的平均误差，使用代价函数来**衡量**假设函数。  
均方根形式的误差函数
<p align='center'>
<img src='https://github.com/jzb1128/Machine_Learning_Notebook/blob/main/image/Cost%20Function.png'>
</p>
