---
layout: default
title: wang-zs的个人网站
description: wang-zs的个人网志
---
<!-- Nav tabs -->
<ul class="nav nav-pills nav-justifiedx">
    <li class="active"><a href="index.md">Home | 首页</a></li>
    <li class=""><a href="/wang-zs-space/archive.html">Archive | 归档</a></li>
</ul>
<hr>
<a href="/ml/tree/index.html">树模型</a>
<br>
<a href="/ml/logister/index.html">逻辑斯特模型</a>
<br>
<a href="/ml/liblinear/index.html">线性回归模型</a>
<br>
<a href="/ml/bayes/index.html">贝叶斯学习</a>
<br>
<a href="/ml/pca/index.html">pca</a>
<br>
<a href="/ml/math/index.html">pca</a>

基本定义：



定量输出称为回归，或者说是连续变量预测；定性输出称为分类，或者说是离散变量预测。

有监督学习（分类，回归）

↕

半监督学习（分类，回归），transductive learning（分类，回归）

↕

半监督聚类（有标签数据的标签不是确定的，类似于：肯定不是xxx，很可能是yyy）

↕

无监督学习（聚类）


交叉验证（一部分样本做训练集，一部分做测试集）的方法 

knn



数学基础

微积分

极限，e，导数，微分，积分

偏导数，方向导数，梯度

极值，多元函数极值，多元函数泰勒展开

无约束优化，约束优化

拉格朗日乘子，对偶问题

 

概率

随机变量，概率密度函数，分布函数

条件概率，全概率公式，贝叶斯公式

期望，方差

大数定理，中心极限定理

协方差，相关系数

常见概率分布，泊松分布

指数族分布，多元高斯分布

参数估计，矩估计，极大似然估计

 

线性代数

矩阵，行列式，初等变换

线性相关，线性无关

秩，特征值，特征向量

正交向量、正交矩阵

矩阵分解

 

机器学习基本概念

输入空间，特征空间和输出空间

联合概率分布，假设空间

三要素：方法=模型+策略+算法

 

感知机Perceptron

感知机模型、学习策略、训练方法

0-1损失函数

感知机的几何解释

感知机证明

pocket perceptron

 

线性回归

模型、损失函数、训练方法、概率解释

  

逻辑回归

模型、损失函数、训练方法、概率解释

逻辑回归的形式，推导和训练，逻辑斯蒂损失

拟牛顿法，LBFGS

  

机器学习诊断和调试

训练误差、测试误差、欠拟合、过拟合

损失函数、风险函数、经验风险、结构风险

正规化、交叉验证

 

推荐系统

协同过滤（User based，Item based，Slope one）

Model-based

SVD++

Aprior算法

 

树模型和boost

熵的定义和应用，信息增益

决策树、ID3、C4.5和CART

Adaboost，指数损失函数

梯度提升树 GBDT

随机森林 Random Forest

 

支持向量机SVM

硬间隔最大化，函数间隔，几何间隔

软间隔最大化

对偶算法

合页损失函数

核函数、核技巧

SMO算法

 

最大熵模型

模型定义、约束条件和推导

重新理解逻辑回归

 

神经网络

模型的定义和训练

BPA算法

 

无监督学习

K-Means和高斯混合模型GMM

EM算法，推导、解释和理解

Topic Model基础，svd、lsa、plsa、lda

 

总结

损失函数比较

模型的比较和选择

解决实际问题的一般步骤



{% include home.html %}
{% include articles.html %}



k近邻算法例子。测试样本（绿色圆形）应归入要么是第一类的蓝色方形或是第二类的红色三角形。如果k=3（实线圆圈）它被分配给第二类，因为有2个三角形和只有1个正方形在内侧圆圈之内。如果k=5（虚线圆圈）它被分配到第一类（3个正方形与2个三角形在外侧圆圈之内）


KNN依然是一种监督学习算法
