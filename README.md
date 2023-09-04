# FTG-LSTM
### Problem definition
![Problem definition](https://github.com/BGMLoveWCJ/FTG-LSTM/blob/main/Introduction/Definition.png)
上面的问题有几种基本的解决方法：\
【1】将序列数据转换成没有前驱后继关系的单个分散的数据点，以此获得一个较大的数据集，使用SVM、Adaboost、XGBoost、DNN可以尝试解决。\
【2】针对序列数据，使用Arima、LSTM、进阶的LSTM、N-Beats等方法。\
【3】数据增强，N较少，可以通过交叉等方式生成一些新的数据。\

经过实验【见code（jupyter）】\
针对【1】，在参考的沃尔玛数据集中表现平平，时间维度的特征比较稀疏（促销活动等），尝试构建很多特征均不能达到好的结果。\
![no for classical]()
针对【2】进阶的LSTM、N-Beats表现也欠佳，也许是数据量比较小的原因，使用【3】中的一些常见序列数据增强方法也不能达到理想的结果。\
反而对于最原始的LSTM，进行合理的分配训练集，可以对沃尔玛最新的销售额有让人有点满意的结果，因此尝试改进LSTM在短序列预测任务中的性能，在几个相关的kaggle竞赛的讨论区得到启发，猜想在小样本的任务中可以采取微调的方式提升LSTM性能。

![proposed architecture]()
![proposed algorithm]()
![comparison]()
