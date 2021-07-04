

### Thinking1： 在CTR点击率预估中，使用GBDT+LR的原理是什么
具有stacking思想的二分类器模型，用来解决二分类问题
通过GBDT将特征进行组合，然后传入给线性分类器
LR对GBDT产生的输入数据进行分类（使用L1正则化防止过拟合）
### Thinking2	GBDT和随机森林都是基于树的算法，它们有什么区别？

随机森林采用的bagging思想，而GBDT采用的boosting思想。
但是都是有放回的抽样，但二者的区别在于：
Bagging采用有放回的均匀取样，而Boosting根据错误率来取样，因此Boosting的分类精度要优于Bagging。
Bagging的训练集的选择是随机的，各训练集之间相互独立，弱分类器可并行，
而Boosting的训练集的选择与前一轮的学习结果有关，是串行的。