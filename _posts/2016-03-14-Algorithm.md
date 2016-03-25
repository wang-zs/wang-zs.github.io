---
title: "机器学习算法-定义与基本"
description: "机器学习"
layout: post
date: 2016-03-14 03:23:44 +0800
thumbnail: http://web.chenjun.com/images/vector_jerry_8ball_by_svezate-d6lzyyh.png
categories: [立占 | site]
tags: [jekyll, github]
comments: yes
---

机器学习的算法：

分类：有指导学习范畴，事先定义类别，类别书不变；(决策树)

聚类：类别在聚类中生成；

监督：

非监督：

半监督：

二元分类与多元分类。


正则化的目的：避免出现过拟合（over-fitting）
经验风险最小化 + 正则化项 = 结构风险最小化
经验风险最小化（ERM），是为了让拟合的误差足够小，即：对训练数据的预测误差很小。
但是，我们学习得到的模型，当然是希望对未知数据有很好的预测能力（泛化能力），这样才更有意义。
当拟合的误差足够小的时候，可能是模型参数较多，模型比较复杂，此时模型的泛化能力一般。于是，我们增加一个正则化项，它是一个正的常数乘以模型复杂度的函数，aJ(f)，a>=0 用于调整ERM与模型复杂度的关系。
结构风险最小化（SRM），相当于是要求拟合的误差足够小，同时模型不要太复杂（正则化项的极小化），这样得到的模型具有较强的泛化能力。
可以去了解奥卡姆剃刀原理（Occam's razor），帮助你理解正则化，实际上是一个道理。

奥卡姆剃刀原理（Occam's razor）：若有多个假设与观察一致，则选最简单的那个。（只是一个假设）


show partitions mp ;

-- 建表语句
CREATE EXTERNAL TABLE `test_subsiby_part_002`(
  `passenger_id` bigint COMMENT '',
  `usual__all` double COMMENT ''
)
COMMENT 'demo外部表'
-- 分区表，分区字段
PARTITIONED BY (
  `year` string,
  `month` string,
  `day` string
)
-- 此处声明字段间分隔符
ROW FORMAT DELIMITED
   FIELDS TERMINATED BY "\t"
-- 此处声明外部表物理数据实际位置
LOCATION
  'hdfs://mycluster-tj/user/wangzhushi/wangzhushi/user_predict/output';
 
 
-- 每次生成新分区数据后，需要声明新分区
ALTER TABLE test_subsiby_part_002 add if not exists partition(year='2016',month='3',day='6') location '2016/3/6';