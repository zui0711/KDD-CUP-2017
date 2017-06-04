# KDD-CUP-2017
KDD CUP 2017 task1

MAPE = 0.1872, 名次 57 / 3754

程序共有三个模型

m1: Pred_big_XGB是直接对整个路段总时间进行预测,使用XGB模型

m2: Pred_cut_XGB是将大路段切分为小路后分别对每个小路段进行预测,然后重组,使用XGB模型

m3: Pred_cut_NN也是将大路段切分后进行预测,使用nn模型


最终成绩由四部分构成:
m1 * 0.5 + (m1' * 0.35 + m2 * 0.35 + m3 * 0.3) * 0.5

m1' * 0.35 + m2 * 0.35 + m3 * 0.3的MAPE = 0.1886
其中m1'为m1的eta取0.05,为中间提交的一个结果

最终线上测评为MAPE = 0.1872
