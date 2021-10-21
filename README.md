# Related work on Database Optimization
Inspired by [GNNPapers](https://github.com/thunlp/GNNPapers).

## Content

* [Conferences&Workshop](#ConferencesWorkshop)
* [Courses](#Courses)
* [Datasets](#Datasets)
* [Tools](#Tools)
* [Papers](#Papers)
  * [Survey papers](#Survey-papers)
  * [Cardinality Estimation](#Cardinality-Estimation)
  * [Selectivity Estimation](#Selectivity-Estimation)
  * [Cost Estimation](#Cost-Estimation)
  * [Query Perfomance Prediction](#Query-Perfomance-Prediction)
  * [Join Order Selection](#Join-Order-Selection)
  * [Query Perfomance Prediction](#Query-Perfomance-Prediction)
  * [Automatic Configuration Tuning](#Automatic-Configuration-Tuning)
  * [Index Tuning](#Index-Tuning)
  * [End-To-End](#End-To-End)
  * [Application](#Application)

## Conferences&Workshop


| Abbreviation                         | Full Name                                                    | -3th                                                | -2th                                                         | -1th                                                         | Latest                                                       |
| ------------------------------------ | :----------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [SIGMOD](https://sigmod.org/)        | International Conference on Management of Data               |                                                     | [2019](https://confer.csail.mit.edu/sigmod2019/schedule#MondayBreakfast) | [2020](https://www.sigmod2020online.org/research/)           | [2021](https://2021.sigmod.org/sigmod_research_list.shtml)   |
| [VLDB](https://www.vldb.org/)        | International Conference on Very large Databases             |                                                     | [2019](https://vldb.org/2019/?papers-research)               | [2020](https://vldb2020.org/program_flat.html)               | [2021](https://vldb.org/2021/?papers-research)               |
| [ICDE](http://ieee-icde.org/)        | International Conference on Data Engineering                 | [2018](https://dblp.org/db/conf/icde/icde2018.html) | [2019](http://conferences.cis.umac.mo/icde2019/?page_id=516) | [2020](https://icde.utdallas.edu/accepted-research-papers.html) | [2021](https://icde2021.gr/accepted-papers/)                 |
| [CIDR](http://cidrdb.org/index.html) | The Conference on Innovative Data Systems Research           |                                                     | [2017](http://cidrdb.org/cidr2017/program.html)              | [2019](http://cidrdb.org/cidr2019/program.html)              | [2020](http://cidrdb.org/cidr2020/program.html)              |
| [EDBT/ICDT](https://www.edbt.org/)   | International Conference on Extending Database Technology    |                                                     | [2018](https://edbticdt2018.at/indexd4d6.html?detailed_program) | [2019](http://edbticdt2019.inesc-id.pt/?detailed_program)    | [2020](https://diku-dk.github.io/edbticdt2020/?contents=detailed_program.html) |
| [DEEM](http://deem-workshop.org/)    | Workshop on Data Management for End-To-End Machine Learning  |                                                     | [2018](http://deem-workshop.org/2018/index.html)             | [2019](http://deem-workshop.org/2019/index.html)             | [2020](http://deem-workshop.org)                             |
| [aiDM](http://www.aidm-conf.org/)    | International Workshop on Exploiting Artificial Intelligence Techniques for Data Management |                                                     | [2018](http://www.aidm-conf.org/aidm_2018.html)              | [2019](http://www.aidm-conf.org/aidm_2019.html)              | [2020](http://www.aidm-conf.org/aidm_2020.html)              |

**Note**: *After entering the resource page, search the keyword to find the corresponding category (such as **optimization**), you can see the receiving papers  under the research category.*


## Courses  
[Advanced Database Systems-CMU-15721-Spring2020](https://15721.courses.cs.cmu.edu/spring2020/)

## Datasets 
[TPC](http://www.tpc.org/)
The TPC Benchmark™H (TPC-H) is a decision support benchmark.

[IMDB](https://www.imdb.com/interfaces/)
Subsets of IMDb data are available for access to customers for personal and non-commercial use.

[JOB](https://github.com/gregrahn/join-order-benchmark)
Join Order Benchmark (JOB).

## Tools 
[TPC-H Query Plan Visualization](https://hyper-db.de/interface.html#)

[SQL AST Explorer](https://astexplorer.net/)

## Papers 
### Survey papers
1. **Synopses for Massive Data: Samples, Histograms, Wavelets, Sketches.** Foundations and Trends in Databases 2012. [book](https://dsf.berkeley.edu/cs286/papers/synopses-fntdb2012.pdf)

	*Graham Cormode, Minos Garofalakis, Peter J. Haas and Chris Jermaine.*
	
1. **How good are query optimizers, really?.** VLDB 2015. [[paper](https://dl.acm.org/doi/pdf/10.14778/2850583.2850594),[github](https://github.com/gregrahn/join-order-benchmark)]

	*Viktor Leis, Andrey Gubichev, Atanas Mirchev, Peter Boncz, Alfons Kemper, and Thomas Neumann.*
	
1. **Database Meets Deep Learning: Challenges and Opportunities.** SIGMOD 2016. [paper](https://dl.acm.org/doi/pdf/10.1145/3003665.3003669)

	*Wei Wang, Meihui Zhang, Gang Chen, H. V. Jagadish, Beng Chin Ooi, and Kian-Lee Tan.*
	
1. **Query optimization through the looking glass, and what we found running the Join Order Benchmark.** The VLDB Journal — The International Journal on Very Large Data Bases 2018. [paper](https://dl.acm.org/doi/pdf/10.1007/s00778-017-0480-7)

	*Viktor Leis, Bernhard Radke, Andrey Gubichev, Atanas Mirchev, Peter Boncz, Alfons Kemper, and Thomas Neumann.*
	
1. **基于机器学习的数据库技术综述.** 计算机学报, 2020. [paper](http://cjc.ict.ac.cn/online/onlinepaper/lgl-2020115164638.pdf)

	*李国良,周煊赫,孙佶,余翔,袁海涛,刘佳斌 ,韩越.*

###  Cardinality Estimation
#### histograms
1. **Equi-depth multidimensional histograms.** SIGMOD 1988. [paper](https://dl.acm.org/doi/pdf/10.1145/50202.50205)

	*M. Muralikrishna and David J. DeWitt.*
	
2. **Selectivity Estimation Without the Attribute Value Independence Assumption.** VLDB 1997. [paper](http://www.vldb.org/conf/1997/P486.PDF)

	*Viswanath Poosala and Yannis E. Ioannidis.*
	
3. **The history of histograms (abridged).** VLDB 2003 . [paper](https://dl.acm.org/doi/pdf/10.5555/1315451.1315455)

	*Yannis Ioannidis.*

#### sketch
1. **A linear-time probabilistic counting algorithm for database applications.** ACM Transactions on Database SystemsJune 1990. [paper](https://dl.acm.org/doi/pdf/10.1145/78922.78925)

	*Kyu-Young Whang, Brad T. Vander-Zanden, and Howard M. Taylor.*
1. **Loglog Counting of Large Cardinalities.** ESA 2003. [paper](http://redisgate.jp/download/DuFl03-LNCS.pdf)

	*Marianne Durand and Philippe Flajolet.*
	
1. **An improved data stream summary: the count-min sketch and its applications.** Journal of Algorithms,Volume 55, Issue 1,2005. [paper](http://pages.di.unipi.it/ferragina/Teach/InformationRetrieval/CMS.pdf)

	*Graham Cormode and S. Muthukrishnan.*
	
1. **HyperLogLog: the analysis of a near-optimal cardinality estimation algorithm.**  Analysis of Algorithms 2007[paper](https://hal.archives-ouvertes.fr/file/index/docid/406166/filename/FlFuGaMe07.pdf)

	*Philippe Flajolet,Éric Fusy,Olivier Gandouet,Frédéric Meunier.*

#### wavelet
1. **Approximate computation of multidimensional aggregates of sparse data using wavelets.** SIGMOD 1999. [paper](https://dl.acm.org/doi/pdf/10.1145/304182.304199)

	*Jeffrey Scott Vitter and Min Wang.*
	
1. **Approximate query processing using wavelets.** The VLDB Journal — The International Journal on Very Large Data BasesSeptember,2001. [paper](https://dl.acm.org/doi/pdf/10.5555/767141.767147)

	*Kaushik Chakrabarti, Minos Garofalakis, Rajeev Rastogi, and Kyuseok Shim.*

#### sampling
1. **Cardinality Estimation Done Right:Index-Based Join Sampling.** CIDR 2017. [paper](http://cidrdb.org/cidr2017/papers/p9-leis-cidr17.pdf)

	*Viktor Leis, B. Radke, Andrey Gubichev, A. Kemper, T. Neumann.*
#### deep learning
1. **Learned Cardinalities:Estimating Correlated Joins with Deep Learning.** CIDR,2019. [[paper](http://cidrdb.org/cidr2019/papers/p101-kipf-cidr19.pdf),[github](https://github.com/andreaskipf/learnedcardinalities)]

    *Andreas Kipf,Thomas Kipfm,Bernhard Radke,Viktor Leis,Peter Boncz,Alfons Kemper.*
    
2. **Estimating Cardinalities with Deep Sketches.** SIGMOD 2019. [paper](https://dl.acm.org/doi/pdf/10.1145/3299869.3320218)
	
	*Andreas Kipf, Dimitri Vorona, Jonas Müller, Thomas Kipf, Bernhard Radke, Viktor Leis, Peter Boncz, Thomas Neumann, and Alfons Kemper.*
	
3. **An end-to-end learning-based cost estimator.** VLDB 2019. [paper](http://www.vldb.org/pvldb/vol13/p307-sun.pdf)

	*Sun Ji, and Guoliang Li.*
	
4. **Monotonic Cardinality Estimation of Similarity Selection: A Deep Learning Approach.** SIGMOD 2020 . [paper](https://dl.acm.org/doi/pdf/10.1145/3318464.3380570)

    *Yaoshu Wang, Chuan Xiao, Jianbin Qin, Xin Cao, Yifang Sun, Wei Wang, and Makoto Onizuka.*

5. **Fauce: Fast and Accurate Deep Ensembles with Uncertainty for Cardinality Estimation.** VLDB 2021.[paper](http://vldb.org/pvldb/vol14/p1950-liu.pdf)

	*Jie Liu, Wenqian Dong, Dong Li, Qingqing Zhou.*

6. **FLAT: Fast, Lightweight and Accurate Method for Cardinality Estimation.** VLDB 2021.[paper](http://vldb.org/pvldb/vol14/p1489-zhu.pdf)

	*Rong Zhu, Ziniu Wu, Yuxing Han, Kai Zeng (Alibaba Group), Andreas Pfadler, Zhengping Qian, Jingren Zhou Bin Cui.*

### Selectivity Estimation
1. **Selectivity Estimation Without the Attribute Value Independence Assumption.** VLDB 1997. [pdf](http://www.vldb.org/conf/1997/P486.PDF)

	*Viswanath Poosala and Yannis E. Ioannidis.*
1. **Selectivity estimation using probabilistic models.** VLDB 2001. [paper](https://dl.acm.org/doi/pdf/10.1145/375663.375727)

	*Lise Getoor, Benjamin Taskar, and Daphne Koller.*
1. **Learning State Representations for Query Optimization with Deep Reinforcement Learning.** DEEM 2018. [paper](https://dl.acm.org/doi/pdf/10.1145/3209889.3209890)

	*Jennifer Ortiz, Magdalena Balazinska, Johannes Gehrke, and S. Sathiya Keerthi.*
	
1. **Deep unsupervised cardinality estimation.** VLDB 2019. [[paper](https://dl.acm.org/doi/pdf/10.14778/3368289.3368294),[github](https://github.com/naru-project/naru)]

	*Zongheng Yang, Eric Liang, Amog Kamsetty, Chenggang Wu, Yan Duan, Xi Chen, Pieter Abbeel, Joseph M. Hellerstein, Sanjay Krishnan, and Ion Stoica.*
	
1. **NeuroCard: one cardinality estimator for all tables.** VLDB 2020. [[paper](https://dl.acm.org/doi/pdf/10.14778/3421424.3421432),[github](https://github.com/naru-project/neurocard)]

	*Zongheng Yang, Amog Kamsetty, Sifei Luan, Eric Liang, Yan Duan, Xi Chen, and Ion Stoica.*
	
1. **Deep Learning Models for Selectivity Estimation of Multi-Attribute Queries.** SIGMOD 2020. [paper](https://dl.acm.org/doi/pdf/10.1145/3318464.3389741)

	*Shohedul Hasan, Saravanan Thirumuruganathan, Jees Augustine, Nick Koudas, and Gautam Das.*

### Cost Estimation
1. **An end-to-end learning-based cost estimator.** VLDB 2019. [[paper](http://www.vldb.org/pvldb/vol13/p307-sun.pdf),[code](https://github.com/TsinghuaDatabaseGroup/AI4DBCode/tree/master/LeanredOptimizer/LearnedCostEstimator))

	*Sun Ji, and Guoliang Li.*

### Join Order Selection
1. **Learning to Optimize Join Queries With Deep Reinforcement Learning.** arxiv 2018. [paper](https://zongheng.me/pubs/dq-jan-2019.pdf)

	*Sanjay Krishnan, Zongheng Yang, Ken Goldberg, Joseph Hellerstein, Ion Stoica.*
	
1. **Deep Reinforcement Learning for Join Order Enumeration.** aiDM 2018 [paper](https://dl.acm.org/doi/pdf/10.1145/3211954.3211957)

	*Ryan Marcus and Olga Papaemmanouil.*
	
1. **Neo: A Learned Query Optimizer.** VLDB 2019. [paper](https://www.cl.cam.ac.uk/~ey204/teaching/ACS/R244_2019_2020/papers/marcus_VLDB_2019.pdf)

	*Ryan Marcus, Parimarjan Negi, Hongzi Mao, Chi Zhang, Mohammad Alizadeh, Tim Kraska, Olga Papaemmanouil, and Nesime Tatbul.*
	
1. **Plan-structured deep neural network models for query performance prediction.** VLDB 2019. [paper](https://dl.acm.org/doi/pdf/10.14778/3342263.3342646)

	*Ryan Marcus and Olga Papaemmanouil.*
	
1. **Research challenges in deep reinforcement learning-based join query optimization.** aiDM 2020. [paper](https://dl.acm.org/doi/pdf/10.1145/3401071.3401657)

	*Runsheng Benson Guo and Khuzaima Daudjee.*
	
1. **Reinforcement Learning with Tree-LSTM for Join Order Selection.** ICDE 2020. [[paper](http://da.qcri.org/ntang/pubs/icde20jos.pdf),[code](https://github.com/TsinghuaDatabaseGroup/AI4DBCode/tree/master/LeanredOptimizer/LeanredJoinOrder/src-RTOS)]

	*Xiang Yu,Guoliang Li,Chengliang Chai and Nan Tang.*
### Query Perfomance Prediction
1. **Query Performance Prediction for Concurrent Queries using Graph Embedding.** VLDB 2020. [paper](http://www.vldb.org/pvldb/vol13/p1416-zhou.pdf)

	*Xuanhe Zhou, Ji Sun, Guoliang Li, Jianhua Feng.*
### Automatic Configuration Tuning
#### statistical approach
1. **Self-tuning performance of database systems based on fuzzy rules.** FSKD'14: 11th International Conference on Fuzzy Systems and Knowledge Discovery ,2014. [paper](https://ieeexplore.ieee.org/abstract/document/6980831)

	*Wei, Zhijie, Zuohua Ding, and Jueliang Hu.*

#### heuristic search
1. **BestConfig: tapping the performance potential of systems via automatic configuration tuning.** SoCC '17: Proceedings of the 2017 Symposium on Cloud Computing, 2017. [paper](https://dl.acm.org/doi/pdf/10.1145/3127479.3128605)
	
	*Yuqing Zhu, Jianxun Liu, Mengying Guo, Yungang Bao, Wenlong Ma, Zhuoyue Liu, Kunpeng Song, and Yingchun Yang.*

#### machine learning
1. **Automatic Database Management System Tuning Through Large-scale Machine Learning.** SIGMOD 2017. [paper](https://dl.acm.org/doi/pdf/10.1145/3035918.3064029)
	
	*Dana Van Aken, Andrew Pavlo, Geoffrey J. Gordon, and Bohan Zhang.*

#### deep learning
1. **An End-to-End Automatic Cloud Database Tuning System Using Deep Reinforcement Learning.** SIGMOD 2019. [paper](https://dl.acm.org/doi/pdf/10.1145/3299869.3300085)
	
	*Ji Zhang, Yu Liu, Ke Zhou, Guoliang Li, Zhili Xiao, Bin Cheng, Jiashu Xing, Yangtao Wang, Tianheng Cheng, Li Liu, Minwei Ran, and Zekang Li.*
### Index tuning
1. **An Adaptive Approach for Index Tuning with Learning Classifier Systems on Hybrid Storage Environments.** HAIS 2018: Hybrid Artificial Intelligent Systems,2018. [paper](https://link.springer.com/chapter/10.1007/978-3-319-92639-1_60)

	*Júlio Cesar NievolaDeborah Carvalho Ribeiro.*
### End-To-End
1. **SkinnerDB: Regret-Bounded Query Evaluation via Reinforcement Learning.** SIGMOD 2019. [paper](https://dl.acm.org/doi/pdf/10.1145/3299869.3300088)

	*Immanuel Trummer, Junxiong Wang, Deepak Maram, Samuel Moseley, Saehan Jo, and Joseph Antonakakis.*
	
1. **Towards a Hands-Free Query Optimizer through Deep Learning.** CIDR 2019. [paper](http://cidrdb.org/cidr2019/papers/p96-marcus-cidr19.pdf)

	*Ryan Marcus and Olga Papaemmanouil.*

### Application
1. **Bao: Making Learned Query Optimization Practical.** SIGMOD 2021. [paper](https://dl.acm.org/doi/pdf/10.1145/3448016.3452838)

	*Ryan Marcus, Parimarjan Negi, Hongzi Mao, Nesime Tatbu, Mohammad Alizadeh, Tim Kraska.*
	
2. **Are We Ready For Learned Cardinality Estimation?**. VLDB 2021. [paper](http://vldb.org/pvldb/vol14/p1640-wang.pdf)

	*Xiaoying Wang, Changbo Qu, Weiyuan Wu, Jiannan Wang, Qingqing Zhou.*