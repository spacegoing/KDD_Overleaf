# Done #

## 文章结构 ##

- review1: In Eq(1) and Eq(2), W and Phi are note defined until
  section 3.2.


## 文章内容 ##

- review1: practical inference time for the proposed method

- review2: To construct the cliques in the MRF, external
  knowledge on the stock groups are required. 这个需要解释

- review3: there is no experiment and evaluation demonstrating
  how the proposed model overcomes the first challenge -
  “Analyzing which groups of stocks will be affected by newly
  arrived information and the corresponding leading stocks”.
  - 第一个challenge不该写leading stocks，另外没有说明白，信息的到
    达可以被价格波动反映出来，不需要分析文本、金融文件

- 应该和intra-clique lead lag ... 相关
- 需要指明mrf中的权重可以encode先验知识
- 添加了0 -1 归为0的金融学引用文献

- review2: 3. How to calculate the technical indicators? Is
  external knowledge required in addition to the stock data set?
  这两个问题原文已经在Table1下方解释过了，是否需要更改位置？

  If not, why the performance on the indicator data set is much
  better than the market dataset? 

- review3: The title of this paper indicates the goal is to
  predict stock prices, but in their experiments, the proposed
  architecture is actually predicing a price movement label which
  is a classification problem.
  - 标题需要改


- review3: The strengths of proposed model in tackling the second
  and third challenge in the experimental evaluation are also
  not clear.
  - 文中应该点名哪些模型、实验解决了哪些challenge

## 实验 ##

- review2: be compared with more baselines, for example, an
  encoder-decoder model; a multi-task baseline where the
  prediction of each stock is regarded as a task;
- review3: The strengths of proposed model in tackling the second
  and third challenge in the experimental evaluation are also
  not clear.
  - 实验中应该点名哪些模型、实验解决了哪些challenge；如何通过对比
    说明


## 看不懂 ##

- review2: The hierarchical multi-task framework seems not necessary. Why not merge the output of DARNN_trent and DARNN_volat tegether into a single vector? Then the hierarchical multi-task DARNN can be replaced with only a single DARNN to simplify the model.
  - 这个会失去multi-task的意义，是不是multi-task的目标（趋势、波
    动）、作用没有写清楚导致别人认为不需要multi-task

- review3: 3. The paper introduces a multi-task DNNs-MRFs
  architecture. However, the Method section fails to discuss the
  multi-task part for this frameworks. 
  - 此处不知是指multi-task的什么没有说清楚，是不是跟上面同样的问
  题
- review3: The HMPL contains three modules of DARNN about how the
  model works to capture informational representations, which is
  not introduced at all.
- review3: It claims the first part learns informative features
  from the raw market data, but the discussion of this part is
  very brief and lacks explanation.
  - 好像跟上面是同一问题
- review3: The connection between this part and the second part,
  MRFs, is also missing which makes the paper not easy to follow
  and reproduce.
  - 如果指的是梯度下降算法，那么文中只给出了梯度求导，因为算法用
    的是引用文献那篇算法，所以只给出了引用文献

# Todo #

## 文章结构 ##

- review1: Some training and evaluation details regarding
  multi-task training as well as end-to-end training provided in
  the supplemental material could be placed into the main
  content.

## 文章内容 ##

- review5: 1) The proposed multi-task framework is novel.
  Actually, I think it can be generally applicable for many time
  series prediction tasks. It is better for the authors to
  introduce some other potential applications in the paper.
  - 是否需要提及计算机视觉中的应用？
- review5: writing, typo需要改

## 实验 ##

- review2: a multi-task baseline where the prediction of each
  stock is regarded as a task;
- review3: The strengths of proposed model in tackling the second
  and third challenge in the experimental evaluation are also
  not clear.
  - 实验中应该点名哪些模型、实验解决了哪些challenge；如何通过对比
    说明


## 看不懂 ##

- review2: The hierarchical multi-task framework seems not necessary. Why not merge the output of DARNN_trent and DARNN_volat tegether into a single vector? Then the hierarchical multi-task DARNN can be replaced with only a single DARNN to simplify the model.
  - 这个会失去multi-task的意义，是不是multi-task的目标（趋势、波
    动）、作用没有写清楚导致别人认为不需要multi-task

- review3: 3. The paper introduces a multi-task DNNs-MRFs
  architecture. However, the Method section fails to discuss the
  multi-task part for this frameworks. 
  - 此处不知是指multi-task的什么没有说清楚，是不是跟上面同样的问
  题
- review3: The HMPL contains three modules of DARNN about how the
  model works to capture informational representations, which is
  not introduced at all.
- review3: It claims the first part learns informative features
  from the raw market data, but the discussion of this part is
  very brief and lacks explanation.
  - 好像跟上面是同一问题
- review3: The connection between this part and the second part,
  MRFs, is also missing which makes the paper not easy to follow
  and reproduce.
  - 如果指的是梯度下降算法，那么文中只给出了梯度求导，因为算法用
    的是引用文献那篇算法，所以只给出了引用文献
