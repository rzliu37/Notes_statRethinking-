
The solution of rethinking statistics is here:
http://xcelab.net/rmpubs/rethinking/rethinking_solutions_2.pdf


# Note_week1


## First section: The Golem of Prague

The first class gives a general overview of this course, like the time schedule and goals.

1. I am impressed by the statement, that statistic models are similar to golem:  statistics just help us to produce inference, it cannot discover the truth, they are just tools we use , sometimes, they work; sometimes, they do not. 


2. Different hypothesis may generate the same statistical models. Therefore, null models are not unique, we should falsify explanatory model, not null model. And we cannot falsify models, but we need to tell them apart from each other. 

3. We need a framework for developing and vetting statistical golems, and this course will provide several options:
(1) Bayesian data analysis
(2) Multilevel modeling
(3) Model comparison

### Bayesian data analysis

* It is all about probability. It will follow these steps: 
* (1)Count all the ways data can happen, accourding to assumptions.
* (2)Assumptions with more ways that are consistent with data are more plausible. 
* 贝叶斯主要是关于概率的问题，主要包括prior distribution和一个posterior distribution。 

### Multilevel models

* Models with multiple levels of uncertainty: replace parameters with models
* Common uses: 1) repear&imbalanced sampling; 2) study variation; 3) avoid averaging; 4)phylogenetics, factor and path analysis, networks, spatical models.
* Natural Bayesian strategy 

### Model comparison

* Basic problems: overfitting; causal inference
* AIC;WAIC;cross-validation
* Must distinguish prediction from inference


## Second section: Garden of Forking data

### 例子: 拿球“三回”

可以考虑拿球问题，已知一个袋子里有四个球，两种颜色，蓝白。有放回的拿球，一共拿了三次，排序为蓝白蓝，推测袋子里的四个球都是什么颜色？

思考逻辑：
* 先把袋子中蓝白球的可能性都写一遍，然后每种可能性都演练一遍，看看每种可能性又会出现多少种“拿三回”的可能性，之后再看符合“蓝白蓝”的有哪些。

* 公式1：

袋子里的可能性：蓝白白白

三回：蓝白蓝

拿到蓝白蓝的可能性：1 x 3 x 1 =3

* 公式2：

袋子里的可能性：蓝蓝白白

三回：蓝白蓝

拿到蓝白蓝的可能性：2 x 2 x 2 =8


* 我对公式的理解：

袋子里有几个蓝球，就用几来相乘，袋子里有几个白球，就用几来相乘。

比如袋子里2蓝2白，蓝白蓝的可能性就是， 2 x 2 x 2 


### 第四回拿球


如果再去那一个球，是蓝色，则可能性会有变动。

* 思考的逻辑顺序是 “三步走”：

1）袋子里的组合有多少种可能性拿出蓝色；

2）之前三个球，“蓝白蓝”，的可能性是多少？

3） 新的可能性是 第一步与第二步相乘

* 应用到题目中

袋子里的可能性：蓝蓝白白

三回：蓝白蓝

第四回：蓝

第一步：2，因为袋子里有两个蓝色

第二步：8，因为蓝白蓝的可能性是，2 x 2 x 2 =8

第三步：16，因为 2 x 8 = 16


### 第五回拿球：工业界说“”

* 蓝色的很稀少，但每个袋子至少有一个

他在ppt中用了“factory account”这一说法，也属于工业信息，如纯白的袋子和纯蓝的袋子都不可能出现，因为蓝色的球虽然少，但至少会有一个

白白白白，0

蓝白白白，3

蓝蓝白白，2

蓝蓝蓝白，1

蓝蓝蓝蓝，0


* 方法是，接着相乘。

如，蓝蓝白白的可能性是：

16 x 2 = 32


### summary

* plausibility is probability: set of non-negative real numbers that sum to one
* procedure: 1) design the model; 2) condition on the data; 3) evaluate the model
* in other words: data story--> updata--> critique




