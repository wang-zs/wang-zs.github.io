---
title: "python工具"
description: "import"
layout: post
date: 2016-03-14 03:23:44 +0800
categories: [工具]
tags: [jekyll, github]
comments: yes
---
import numpy as np; import pandas as pd;

test code:注意不要泄露数据
贾倚天数据比较：
df_jia = pd.read_csv('shenzheng_jia_20160101_20160129', header=None, delimiter='\t')
df_my = pd.read_csv('peace.01', delimiter='\t')

my_oid = (df_my.values)[:, 0]
jia_oid = (df_jia.values)[:, 2]

res = np.setdiff1d(my_oid, jia_oid)
# res_test = np.setdiff1d(jia_oid, my_oid)
# res_test.shape[0] == 0
