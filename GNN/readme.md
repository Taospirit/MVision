# 图卷积网络（Graph Convolutional Network） 因果推理
[相关论文](https://github.com/Ewenwan/GNNPapers)

[代码](https://github.com/Ewenwan/Graph-neural-networks)

[简介](https://tkipf.github.io/graph-convolutional-networks/)

[Deep Learning on Graphs with Graph Convolutional Networks](http://deeploria.gforge.inria.fr/thomasTalk.pdf)

[Relational inductive biases, deep learning, and graph networks](https://arxiv.org/pdf/1806.01261.pdf)

[新奇网络](https://github.com/jungwonkang/references/wiki/Deep-Etc)

      图（graph）是一种数据格式，它可以用于表示社交网络、通信网络、蛋白分子网络等，
      图中的节点表示网络中的个体，连边表示个体之间的连接关系。
      许多机器学习任务例如社团发现、链路预测等都需要用到图结构数据，
      因此图卷积神经网络的出现为这些问题的解决提供了新的思路。
[清华大学孙茂松组一文综述GNN](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652034713&idx=1&sn=66be74a9435810f1e782bc0de44b3791&chksm=f121a268c6562b7e9d3905468b6995427b689fe580c3283ada699f1b928236aeb771f15eb91c&mpshare=1&scene=23&srcid=12278Oi7f7bFQuHybgt0xvBU#rd)

      
      深度学习无法进行因果推理，而图模型(GNN)或是解决方案之一。
      图神经网络是连接主义与符号主义的有机结合，
      不仅使深度学习模型能够应用在图这种非欧几里德结构上，
      还为深度学习模型赋予了一定的因果推理能力。

## GNN的三大通用框架
      1. 消息传递神经网络(message passing neural network， MPNN)，统一了各种 图神经网络 和 图卷积网络方法。
      2. 非局部神经网络(non-local neural network, NLNN)，它结合了几种“self-attention”风格的方法。
      3. 图网络(graph network, GN)，它统一了统一了MPNN和NLNN方法以及许多其他变体，
         如交互网络(Interaction Networks)，
         神经物理引擎(Neural Physics Engine)，
         CommNet，structure2vec，
         GGNN，
         关系网络(Relation Network)，
         Deep Sets 和
         Point Net。
## 问题
      1. GNN总是很浅，大多数不超过三层。
         堆叠多个GCN层将导致过度平滑，也就是说，所有顶点将收敛到相同的值。
         
      2. GNN在非结构场景中的应用。
      
      3. 对GNN进行扩展是很困难的。
         首先，图数据并不规则，每个节点都有自己的邻域结构，因此不能批量化处理。
         其次，当存在的节点和边数量达到数百万时，计算图的拉普拉斯算子也是不可行的。
         此外，我们需要指出，可扩展性的高低，决定了算法是否能够应用于实际场景。
         目前已经有一些研究提出了解决这个问题的办法，我们正在密切关注这些新进展。
         



## 综述研究类论文
1. **Graph Neural Networks: A Review of Methods and Applications.**
*Jie Zhou, Ganqu Cui, Zhengyan Zhang, Cheng Yang, Zhiyuan Liu, Maosong Sun.* 2018. [paper](https://arxiv.org/pdf/1812.08434.pdf)

2. **Deep Learning on Graphs: A Survey.**
*Ziwei Zhang, Peng Cui, Wenwu Zhu.* 2018. [paper](https://arxiv.org/pdf/1812.04202.pdf)

3. **Relational Inductive Biases, Deep Learning, and Graph Networks.**
*Battaglia, Peter W and Hamrick, Jessica B and Bapst, Victor and Sanchez-Gonzalez, Alvaro and Zambaldi, Vinicius and Malinowski, Mateusz and Tacchetti, Andrea and Raposo, David and Santoro, Adam and Faulkner, Ryan and others.* 2018. [paper](https://arxiv.org/pdf/1806.01261.pdf)

4. **Geometric Deep Learning: Going beyond Euclidean data.**
*Bronstein, Michael M and Bruna, Joan and LeCun, Yann and Szlam, Arthur and Vandergheynst, Pierre.* IEEE SPM 2017. [paper](https://arxiv.org/pdf/1611.08097.pdf)

5. **Computational Capabilities of Graph Neural Networks.**
*Scarselli, Franco and Gori, Marco and Tsoi, Ah Chung and Hagenbuchner, Markus and Monfardini, Gabriele.* IEEE TNN 2009. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4703190)

6. **Neural Message Passing for Quantum Chemistry.**
*Gilmer, Justin and Schoenholz, Samuel S and Riley, Patrick F and Vinyals, Oriol and Dahl, George E.* 2017. [paper](https://arxiv.org/pdf/1704.01212.pdf)

7. **Non-local Neural Networks.**
*Wang, Xiaolong and Girshick, Ross and Gupta, Abhinav and He, Kaiming.* CVPR 2018. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Non-Local_Neural_Networks_CVPR_2018_paper.pdf)

8. **The Graph Neural Network Model.**
*Scarselli, Franco and Gori, Marco and Tsoi, Ah Chung and Hagenbuchner, Markus and Monfardini, Gabriele.* IEEE TNN 2009. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4700287)


## 模型
1. **A new model for learning in graph domains.**
*Marco Gori, Gabriele Monfardini, Franco Scarselli.* IJCNN 2005. [paper](https://www.researchgate.net/profile/Franco_Scarselli/publication/4202380_A_new_model_for_earning_in_raph_domains/links/0c9605188cd580504f000000.pdf)

1. **Graph Neural Networks for Ranking Web Pages.**
*Franco Scarselli, Sweah Liang Yong, Marco Gori, Markus Hagenbuchner, Ah Chung Tsoi, Marco Maggini.* WI 2005. [paper](https://www.researchgate.net/profile/Franco_Scarselli/publication/221158677_Graph_Neural_Networks_for_Ranking_Web_Pages/links/0c9605188cd5090ede000000/Graph-Neural-Networks-for-Ranking-Web-Pages.pdf)

1. **Gated Graph Sequence Neural Networks.**
*Yujia Li, Daniel Tarlow, Marc Brockschmidt, Richard Zemel.* ICLR 2016. [paper](https://arxiv.org/pdf/1511.05493.pdf)

1. **Geometric deep learning on graphs and manifolds using mixture model cnns.**
*Federico Monti, Davide Boscaini, Jonathan Masci, Emanuele Rodolà, Jan Svoboda, Michael M. Bronstein.* CVPR 2017. [paper](https://arxiv.org/pdf/1611.08402.pdf)

1. **Spectral Networks and Locally Connected Networks on Graphs.**
*Joan Bruna, Wojciech Zaremba, Arthur Szlam, Yann LeCun.* ICLR 2014. [paper](https://arxiv.org/pdf/1312.6203.pdf)

1. **Deep Convolutional Networks on Graph-Structured Data.**
*Mikael Henaff, Joan Bruna, Yann LeCun.* 2015. [paper](https://arxiv.org/pdf/1506.05163.pdf)

1. **Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering.**
*Michaël Defferrard, Xavier Bresson, Pierre Vandergheynst.* NIPS 2016. [paper](http://papers.nips.cc/paper/6081-convolutional-neural-networks-on-graphs-with-fast-localized-spectral-filtering.pdf)

1. **Learning Convolutional Neural Networks for Graphs.**
*Mathias Niepert, Mohamed Ahmed, Konstantin Kutzkov.* ICML 2016. [paper](http://proceedings.mlr.press/v48/niepert16.pdf)

1. **Semi-Supervised Classification with Graph Convolutional Networks.**
*Thomas N. Kipf, Max Welling.* ICLR 2017. [paper](https://arxiv.org/pdf/1609.02907.pdf)

1. **Graph Attention Networks.**
*Petar Velickovic, Guillem Cucurull, Arantxa Casanova, Adriana Romero, Pietro Lio, Yoshua Bengio.* ICLR 2018. [paper](https://mila.quebec/wp-content/uploads/2018/07/d1ac95b60310f43bb5a0b8024522fbe08fb2a482.pdf)

1. **Deep Sets.**
*Manzil Zaheer, Satwik Kottur, Siamak Ravanbakhsh, Barnabas Poczos, Ruslan Salakhutdinov, Alexander Smola.* NIPS 2017. [paper](https://arxiv.org/pdf/1703.06114.pdf)

1. **Graph Partition Neural Networks for Semi-Supervised Classification.**
*Renjie Liao, Marc Brockschmidt, Daniel Tarlow, Alexander L. Gaunt, Raquel Urtasun, Richard Zemel.* 2018. [paper](https://arxiv.org/pdf/1803.06272.pdf)

1. **Covariant Compositional Networks For Learning Graphs.**
*Risi Kondor, Hy Truong Son, Horace Pan, Brandon Anderson, Shubhendu Trivedi.* 2018. [paper](https://arxiv.org/pdf/1801.02144.pdf)

1. **Modeling Relational Data with Graph Convolutional Networks.**
*Michael Schlichtkrull, Thomas N. Kipf, Peter Bloem, Rianne van den Berg, Ivan Titov, Max Welling.* ESWC 2018. [paper](https://arxiv.org/pdf/1703.06103.pdf)

1. **Stochastic Training of Graph Convolutional Networks with Variance Reduction.**
*Jianfei Chen, Jun Zhu, Le Song.* ICML 2018. [paper](http://www.scipaper.net/uploadfile/2018/0716/20180716100330880.pdf)

1. **Learning Steady-States of Iterative Algorithms over Graphs.**
*Hanjun Dai, Zornitsa Kozareva, Bo Dai, Alex Smola, Le Song.* ICML 2018. [paper](http://proceedings.mlr.press/v80/dai18a/dai18a.pdf)

1. **Deriving Neural Architectures from Sequence and Graph Kernels.**
*Tao Lei, Wengong Jin, Regina Barzilay, Tommi Jaakkola.* ICML 2017. [paper](https://arxiv.org/pdf/1705.09037.pdf)

1. **Adaptive Graph Convolutional Neural Networks.**
*Ruoyu Li, Sheng Wang, Feiyun Zhu, Junzhou Huang.* AAAI 2018. [paper](https://arxiv.org/pdf/1801.03226.pdf)

1. **Graph-to-Sequence Learning using Gated Graph Neural Networks.**
*Daniel Beck, Gholamreza Haffari, Trevor Cohn.* ACL 2018. [paper](https://arxiv.org/pdf/1806.09835.pdf)

1. **Deeper Insights into Graph Convolutional Networks for Semi-Supervised Learning.**
*Qimai Li, Zhichao Han, Xiao-Ming Wu.* AAAI 2018. [paper](https://arxiv.org/pdf/1801.07606.pdf)

1. **Graphical-Based Learning Environments for Pattern Recognition.**
*Franco Scarselli, Ah Chung Tsoi, Marco Gori, Markus Hagenbuchner.* SSPR/SPR 2004. [paper](https://link.springer.com/content/pdf/10.1007%2F978-3-540-27868-9_4.pdf)

1. **A Comparison between Recursive Neural Networks and Graph Neural Networks.**
*Vincenzo Di Massa, Gabriele Monfardini, Lorenzo Sarti, Franco Scarselli, Marco Maggini, Marco Gori.* IJCNN 2006. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1716174)

1. **Graph Neural Networks for Object Localization.**
*Gabriele Monfardini, Vincenzo Di Massa, Franco Scarselli, Marco Gori.* ECAI 2006. [paper](http://ebooks.iospress.nl/volumearticle/2775)

1. **Knowledge-Guided Recurrent Neural Network Learning for Task-Oriented Action Prediction.**
*Liang Lin, Lili Huang, Tianshui Chen, Yukang Gan, Hui Cheng.* ICME 2017. [paper](https://arxiv.org/pdf/1707.04677.pdf)

1. **Semantic Object Parsing with Graph LSTM.**
*Xiaodan LiangXiaohui ShenJiashi FengLiang Lin, Shuicheng Yan.* ECCV 2016. [paper](https://link.springer.com/content/pdf/10.1007%2F978-3-319-46448-0_8.pdf)

1. **CelebrityNet: A Social Network Constructed from Large-Scale Online Celebrity Images.**
*Li-Jia Li, David A. Shamma, Xiangnan Kong, Sina Jafarpour, Roelof Van Zwol, Xuanhui Wang.* TOMM 2015. [paper](https://dl.acm.org/ft_gateway.cfm?id=2801125&ftid=1615097&dwn=1&CFID=38275959&CFTOKEN=6938a464cf972252-DF065FDC-9FED-EB68-3528017EA04F0D29)

1. **Inductive Representation Learning on Large Graphs.**
*William L. Hamilton, Rex Ying, Jure Leskovec.* NIPS 2017. [paper](https://arxiv.org/pdf/1706.02216.pdf)

1. **Graph Classification using Structural Attention.**
*John Boaz Lee, Ryan Rossi, Xiangnan Kong.* KDD 18. [paper](https://dl.acm.org/ft_gateway.cfm?id=3219980&ftid=1988883&dwn=1&CFID=38275959&CFTOKEN=6938a464cf972252-DF065FDC-9FED-EB68-3528017EA04F0D29)

1. **Adversarial Attacks on Neural Networks for Graph Data.**
*Daniel Zügner, Amir Akbarnejad, Stephan Günnemann.* KDD 18. [paper](http://delivery.acm.org/10.1145/3230000/3220078/p2847-zugner.pdf?ip=101.5.139.169&id=3220078&acc=ACTIVE%20SERVICE&key=BF85BBA5741FDC6E%2E587F3204F5B62A59%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1545706391_e7484be677293ffb5f18b39ce84a0df9)

1. **Large-Scale Learnable Graph Convolutional Networks.**
*Hongyang Gao, Zhengyang Wang, Shuiwang Ji.* KDD 18. [paper](http://delivery.acm.org/10.1145/3220000/3219947/p1416-gao.pdf?ip=101.5.139.169&id=3219947&acc=ACTIVE%20SERVICE&key=BF85BBA5741FDC6E%2E587F3204F5B62A59%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1545706457_bb20316c7ce038aefb97afcf4ef9668b)

1. **Contextual Graph Markov Model: A Deep and Generative Approach to Graph Processing.**
*Davide Bacciu, Federico Errica, Alessio Micheli.* ICML 2018. [paper](https://arxiv.org/pdf/1805.10636.pdf)

1. **Diffusion-Convolutional Neural Networks.**
*James Atwood, Don Towsley.* NIPS 2016. [paper](https://arxiv.org/pdf/1511.02136.pdf)

1. **Neural networks for relational learning: an experimental comparison.**
*Werner Uwents, Gabriele Monfardini, Hendrik Blockeel, Marco Gori, Franco Scarselli.* Machine Learning 2011. [paper](https://link.springer.com/content/pdf/10.1007%2Fs10994-010-5196-5.pdf)

1. **FastGCN: Fast Learning with Graph Convolutional Networks via Importance Sampling.**
*Jie Chen, Tengfei Ma, Cao Xiao.* ICLR 2018. [paper](https://arxiv.org/pdf/1801.10247.pdf)

1. **Adaptive Sampling Towards Fast Graph Representation Learning.**
*Wenbing Huang, Tong Zhang, Yu Rong, Junzhou Huang.* NIPS 2018. [paper](https://arxiv.org/pdf/1809.05343.pdf)

## 应用

1. **Discovering objects and their relations from entangled scene representations.**
*David Raposo, Adam Santoro, David Barrett, Razvan Pascanu, Timothy Lillicrap, Peter Battaglia.* ICLR Workshop 2017. [paper](https://arxiv.org/pdf/1702.05068.pdf)

1. **A simple neural network module for relational reasoning.**
*Adam Santoro, David Raposo, David G.T. Barrett, Mateusz Malinowski, Razvan Pascanu, Peter Battaglia, Timothy Lillicrap.* NIPS 2017. [paper](https://arxiv.org/pdf/1706.01427.pdf)

1. **Attend, Infer, Repeat: Fast Scene Understanding with Generative Models.**
*S. M. Ali Eslami, Nicolas Heess, Theophane Weber, Yuval Tassa, David Szepesvari, Koray Kavukcuoglu, Geoffrey E. Hinton.* NIPS 2016. [paper](https://arxiv.org/pdf/1603.08575.pdf)

1. **Beyond Categories: The Visual Memex Model for Reasoning About Object Relationships.**
*Tomasz Malisiewicz, Alyosha Efros.* NIPS 2009. [paper](http://papers.nips.cc/paper/3647-beyond-categories-the-visual-memex-model-for-reasoning-about-object-relationships.pdf)

1. **Understanding Kin Relationships in a Photo.**
*Siyu Xia, Ming Shao, Jiebo Luo, Yun Fu.* TMM 2012. [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6151163)

1. **Graph-Structured Representations for Visual Question Answering.**
*Damien Teney, Lingqiao Liu, Anton van den Hengel.* CVPR 2017. [paper](https://arxiv.org/pdf/1609.05600.pdf)

1. **Spatial Temporal Graph Convolutional Networks for Skeleton-Based Action Recognition.**
*Sijie Yan, Yuanjun Xiong, Dahua Lin.* AAAI 2018. [paper](https://arxiv.org/pdf/1801.07455.pdf)

1. **Few-Shot Learning with Graph Neural Networks.**
*Victor Garcia, Joan Bruna.* ICLR 2018. [paper](https://arxiv.org/pdf/1711.04043.pdf)

1. **The More You Know: Using Knowledge Graphs for Image Classification.**
*Kenneth Marino, Ruslan Salakhutdinov, Abhinav Gupta.* CVPR 2017. [paper](https://arxiv.org/pdf/1612.04844.pdf)

1. **Zero-shot Recognition via Semantic Embeddings and Knowledge Graphs.**
*Xiaolong Wang, Yufei Ye, Abhinav Gupta.* CVPR 2018. [paper](https://arxiv.org/pdf/1803.08035.pdf)

1. **Rethinking Knowledge Graph Propagation for Zero-Shot Learning.**
*Michael Kampffmeyer, Yinbo Chen, Xiaodan Liang, Hao Wang, Yujia Zhang, Eric P. Xing.* 2018. [paper](https://arxiv.org/pdf/1805.11724.pdf)

1. **Interaction Networks for Learning about Objects, Relations and Physics.**
*Peter Battaglia, Razvan Pascanu, Matthew Lai, Danilo Rezende, Koray Kavukcuoglu.* NIPS 2016. [paper](https://arxiv.org/pdf/1612.00222.pdf)

1. **A Compositional Object-Based Approach to Learning Physical Dynamics.**
*Michael B. Chang, Tomer Ullman, Antonio Torralba, Joshua B. Tenenbaum.* ICLR 2017. [paper](https://arxiv.org/pdf/1612.00341.pdf)

1. **Visual Interaction Networks: Learning a Physics Simulator from Vide.o** 
*Nicholas Watters, Andrea Tacchetti, Théophane Weber, Razvan Pascanu, Peter Battaglia, Daniel Zoran.* NIPS 2017. [paper](http://papers.nips.cc/paper/7040-visual-interaction-networks-learning-a-physics-simulator-from-video.pdf)

1. **Relational neural expectation maximization: Unsupervised discovery of objects and their interactions.**
*Sjoerd van Steenkiste, Michael Chang, Klaus Greff, Jürgen Schmidhuber.* ICLR 2018. [paper](https://arxiv.org/pdf/1802.10353.pdf)

1. **Graph networks as learnable physics engines for inference and control.**
*Alvaro Sanchez-Gonzalez, Nicolas Heess, Jost Tobias Springenberg, Josh Merel, Martin Riedmiller, Raia Hadsell, Peter Battaglia.* ICML 2018. [paper](https://arxiv.org/pdf/1806.01242.pdf)

1. **Learning Multiagent Communication with Backpropagation.**
*Sainbayar Sukhbaatar, Arthur Szlam, Rob Fergus.* NIPS 2016. [paper](https://arxiv.org/pdf/1605.07736.pdf)

1. **VAIN: Attentional Multi-agent Predictive Modeling.**
*Yedid Hoshen.* NIPS 2017 [paper](https://arxiv.org/pdf/1706.06122.pdf)

1. **Neural Relational Inference for Interacting Systems.**
*Thomas Kipf, Ethan Fetaya, Kuan-Chieh Wang, Max Welling, Richard Zemel.* ICML 2018. [paper](https://arxiv.org/pdf/1802.04687.pdf)

1. **Translating Embeddings for Modeling Multi-relational Data.**
*Antoine Bordes, Nicolas Usunier, Alberto Garcia-Duran, Jason Weston, Oksana Yakhnenko.* NIPS 2013. [paper](http://papers.nips.cc/paper/5071-translating-embeddings-for-modeling-multi-relational-data.pdf)

1. **Representation learning for visual-relational knowledge graphs.**
*Daniel Oñoro-Rubio, Mathias Niepert, Alberto García-Durán, Roberto González, Roberto J. López-Sastre.* 2017. [paper](https://arxiv.org/pdf/1709.02314.pdf)

1. **Knowledge Transfer for Out-of-Knowledge-Base Entities : A Graph Neural Network Approach.**
*Takuo Hamaguchi, Hidekazu Oiwa, Masashi Shimbo, Yuji Matsumoto.* IJCAI 2017. [paper](https://arxiv.org/pdf/1706.05674.pdf)

1. **Representation Learning on Graphs with Jumping Knowledge Networks.**
*Keyulu Xu, Chengtao Li, Yonglong Tian, Tomohiro Sonobe, Ken-ichi Kawarabayashi, Stefanie Jegelka.* ICML 2018. [paper](https://arxiv.org/pdf/1806.03536.pdf)

1. **Multi-Label Zero-Shot Learning with Structured Knowledge Graphs.**
*Chung-Wei Lee, Wei Fang, Chih-Kuan Yeh, Yu-Chiang Frank Wang.* CVPR 2018. [paper](https://arxiv.org/pdf/1711.06526.pdf)

1. **Dynamic Graph Generation Network: Generating Relational Knowledge from Diagrams.**
*Daesik Kim, Youngjoon Yoo, Jeesoo Kim, Sangkuk Lee, Nojun Kwak.* CVPR 2018. [paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/Kim_Dynamic_Graph_Generation_CVPR_2018_paper.pdf)

1. **Deep Reasoning with Knowledge Graph for Social Relationship Understanding.**
*Zhouxia Wang, Tianshui Chen, Jimmy Ren, Weihao Yu, Hui Cheng, Liang Lin.* IJCAI 2018. [paper](https://arxiv.org/pdf/1807.00504.pdf)

1. **Constructing Narrative Event Evolutionary Graph for Script Event Prediction.**
*Zhongyang Li, Xiao Ding, Ting Liu.* IJCAI 2018. [paper](https://arxiv.org/pdf/1805.05081.pdf)

1. **Modeling Semantics with Gated Graph Neural Networks for Knowledge Base Question Answering.**
*Daniil Sorokin, Iryna Gurevych.* COLING 2018. [paper](https://arxiv.org/pdf/1808.04126.pdf)

1. **Convolutional networks on graphs for learning molecular fingerprints.**
*David Duvenaud, Dougal Maclaurin, Jorge Aguilera-Iparraguirre, Rafael Gómez-Bombarelli, Timothy Hirzel, Alán Aspuru-Guzik, Ryan P. Adams.* NIPS 2015. [paper](https://arxiv.org/pdf/1509.09292.pdf)

1. **Molecular Graph Convolutions: Moving Beyond Fingerprints.**
*Steven Kearnes, Kevin McCloskey, Marc Berndl, Vijay Pande, Patrick Riley.* Journal of computer-aided molecular design 2016. [paper](https://arxiv.org/pdf/1603.00856.pdf)

1. **Protein Interface Prediction using Graph Convolutional Networks.**
*Alex Fout, Jonathon Byrd, Basir Shariat, Asa Ben-Hur.* NIPS 2017. [paper](http://papers.nips.cc/paper/7231-protein-interface-prediction-using-graph-convolutional-networks.pdf)

1. **Traffic Graph Convolutional Recurrent Neural Network: A Deep Learning Framework for Network-Scale Traffic Learning and Forecasting.**
*Zhiyong Cui, Kristian Henrickson, Ruimin Ke, Yinhai Wang.* 2018. [paper](https://arxiv.org/pdf/1802.07007.pdf)

1. **Spatio-Temporal Graph Convolutional Networks: A Deep Learning Framework for Traffic Forecasting.**
*Bing Yu, Haoteng Yin, Zhanxing Zhu.* IJCAI 2018. [paper](https://arxiv.org/pdf/1709.04875.pdf)

1. **Semi-supervised User Geolocation via Graph Convolutional Networks.**
*Afshin Rahimi, Trevor Cohn, Timothy Baldwin.* ACL 2018. [paper](https://arxiv.org/pdf/1804.08049.pdf)

1. **Dynamic Graph CNN for Learning on Point Clouds.**
*Yue Wang, Yongbin Sun, Ziwei Liu, Sanjay E. Sarma, Michael M. Bronstein, Justin M. Solomon.* CVPR 2018. [paper](https://arxiv.org/pdf/1801.07829.pdf)

1. **PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation.**
*Charles R. Qi, Hao Su, Kaichun Mo, Leonidas J. Guibas.* CVPR 2018. [paper](https://arxiv.org/pdf/1612.00593.pdf)

1. **3D Graph Neural Networks for RGBD Semantic Segmentation.**
*Xiaojuan Qi, Renjie Liao, Jiaya Jia, Sanja Fidler, Raquel Urtasun.* CVPR 2017. [paper](http://openaccess.thecvf.com/content_ICCV_2017/papers/Qi_3D_Graph_Neural_ICCV_2017_paper.pdf)

1. **Iterative Visual Reasoning Beyond Convolutions.**
*Xinlei Chen, Li-Jia Li, Li Fei-Fei, Abhinav Gupta.* CVPR 2018. [paper](https://arxiv.org/pdf/1803.11189)

1. **Dynamic Edge-Conditioned Filters in Convolutional Neural Networks on Graphs.**
*Martin Simonovsky, Nikos Komodakis.* CVPR 2017. [paper](https://arxiv.org/pdf/1704.02901)

1. **Situation Recognition with Graph Neural Networks.**
*Ruiyu Li, Makarand Tapaswi, Renjie Liao, Jiaya Jia, Raquel Urtasun, Sanja Fidler.* ICCV 2017. [paper](https://arxiv.org/pdf/1708.04320)

1. **Conversation Modeling on Reddit using a Graph-Structured LSTM.**
*Vicky Zayats, Mari Ostendorf.* TACL 2018. [paper](https://arxiv.org/pdf/1704.02080)

1. **Graph Convolutional Networks for Text Classification.**
*Liang Yao, Chengsheng Mao, Yuan Luo.* AAAI 2019. [paper](https://arxiv.org/pdf/1809.05679.pdf)

1. **Attention Is All You Need.**
*Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin.* NIPS 2017. [paper](https://arxiv.org/pdf/1706.03762)

1. **Self-Attention with Relative Position Representations.**
*Peter Shaw, Jakob Uszkoreit, Ashish Vaswani.* NAACL 2018. [paper](https://arxiv.org/pdf/1803.02155)

1. **Hyperbolic Attention Networks.**
*Caglar Gulcehre, Misha Denil, Mateusz Malinowski, Ali Razavi, Razvan Pascanu, Karl Moritz Hermann, Peter Battaglia, Victor Bapst, David Raposo, Adam Santoro, Nando de Freitas* 2018. [paper](https://arxiv.org/pdf/1805.09786)

1. **Effective Approaches to Attention-based Neural Machine Translation.**
*Minh-Thang Luong, Hieu Pham, Christopher D. Manning.* EMNLP 2015. [paper](https://arxiv.org/pdf/1508.04025)

1. **Graph Convolutional Encoders for Syntax-aware Neural Machine Translation.**
*Joost Bastings, Ivan Titov, Wilker Aziz, Diego Marcheggiani, Khalil Sima'an.* EMNLP 2017. [paper](https://arxiv.org/pdf/1704.04675)

1. **NerveNet: Learning Structured Policy with Graph Neural Networks.**
*Tingwu Wang, Renjie Liao, Jimmy Ba, Sanja Fidler.* ICLR 2018. [paper](https://openreview.net/pdf?id=S1sqHMZCb)

1. **Metacontrol for Adaptive Imagination-Based Optimization.**
*Jessica B. Hamrick, Andrew J. Ballard, Razvan Pascanu, Oriol Vinyals, Nicolas Heess, Peter W. Battaglia.* ICLR 2017. [paper](https://arxiv.org/pdf/1705.02670)

1. **Learning model-based planning from scratch.**
*Razvan Pascanu, Yujia Li, Oriol Vinyals, Nicolas Heess, Lars Buesing, Sebastien Racanière, David Reichert, Théophane Weber, Daan Wierstra, Peter Battaglia.* 2017. [paper](https://arxiv.org/pdf/1707.06170)

1. **Structured Dialogue Policy with Graph Neural Networks.**
*Lu Chen, Bowen Tan, Sishan Long and Kai Yu.* ICCL 2018. [paper](http://www.aclweb.org/anthology/C18-1107)

1. **Relational inductive bias for physical construction in humans and machines.**
*Jessica B. Hamrick, Kelsey R. Allen, Victor Bapst, Tina Zhu, Kevin R. McKee, Joshua B. Tenenbaum, Peter W. Battaglia.* CogSci 2018. [paper](https://arxiv.org/abs/1806.01203)

1. **Relational Deep Reinforcement Learning.**
*Vinicius Zambaldi, David Raposo, Adam Santoro, Victor Bapst, Yujia Li, Igor Babuschkin, Karl Tuyls, David Reichert, Timothy Lillicrap, Edward Lockhart, Murray Shanahan, Victoria Langston, Razvan Pascanu, Matthew Botvinick, Oriol Vinyals, Peter Battaglia.* 2018. [paper](https://arxiv.org/abs/1806.01830)

1. **Action Schema Networks: Generalised Policies with Deep Learning.**
*Sam Toyer, Felipe Trevizan, Sylvie Thiébaux, Lexing Xie.* AAAI 2018. [paper](https://arxiv.org/abs/1709.04271)

1. **Neural Combinatorial Optimization with Reinforcement Learning.**
*Irwan Bello, Hieu Pham, Quoc V. Le, Mohammad Norouzi, Samy Bengio.* 2016. [paper](https://arxiv.org/abs/1611.09940)

1. **A Note on Learning Algorithms for Quadratic Assignment with Graph Neural Networks.**
*Alex Nowak, Soledad Villar, Afonso S. Bandeira, Joan Bruna.* PADL 2017. [paper](https://www.padl.ws/papers/Paper%2017.pdf)

1. **Learning Combinatorial Optimization Algorithms over Graphs.**
*Hanjun Dai, Elias B. Khalil, Yuyu Zhang, Bistra Dilkina, Le Song.* NIPS 2017. [paper](https://arxiv.org/abs/1704.01665)

1. **Attention Solves Your TSP, Approximately.**
*Wouter Kool, Herke van Hoof, Max Welling.* 2018. [paper](https://arxiv.org/abs/1803.08475)

1. **Learning a SAT Solver from Single-Bit Supervision.**
*Daniel Selsam, Matthew Lamm, Benedikt Bünz, Percy Liang, Leonardo de Moura, David L. Dill.* 2018. [paper](https://arxiv.org/abs/1802.03685)

1. **Learning to Represent Programs with Graphs.**
*Miltiadis Allamanis, Marc Brockschmidt, Mahmoud Khademi.* ICLR 2018. [paper](https://arxiv.org/abs/1711.00740)

1. **Learning Graphical State Transitions.**
*Daniel D. Johnson.* ICLR 2017. [paper](https://openreview.net/forum?id=HJ0NvFzxl)

1. **Inference in Probabilistic Graphical Models by Graph Neural Networks.**
*KiJung Yoon, Renjie Liao, Yuwen Xiong, Lisa Zhang, Ethan Fetaya, Raquel Urtasun, Richard Zemel, Xaq Pitkow.* ICLR Workshop 2018. [paper](https://arxiv.org/abs/1803.07710)

1. **Learning deep generative models of graphs.**
*Yujia Li, Oriol Vinyals, Chris Dyer, Razvan Pascanu, Peter Battaglia.* ICLR Workshop 2018. [paper](https://arxiv.org/abs/1803.03324)

1. **MolGAN: An implicit generative model for small molecular graphs.**
*Nicola De Cao, Thomas Kipf.* 2018. [paper](https://arxiv.org/abs/1805.11973)

1. **GraphRNN: Generating Realistic Graphs with Deep Auto-regressive Models.**
*Jiaxuan You, Rex Ying, Xiang Ren, William L. Hamilton, Jure Leskovec.* ICML 2018. [paper](https://arxiv.org/abs/1802.08773)

1. **NetGAN: Generating Graphs via Random Walks.**
*Aleksandar Bojchevski, Oleksandr Shchur, Daniel Zügner, Stephan Günnemann.* ICML 2018. [paper](https://arxiv.org/abs/1803.00816)

1. **Adversarial Attack on Graph Structured Data.**
*Hanjun Dai, Hui Li, Tian Tian, Xin Huang, Lin Wang, Jun Zhu, Le Song.* ICML 2018. [paper](https://arxiv.org/abs/1806.02371)

1. **Graph Convolutional Neural Networks for Web-Scale Recommender Systems.**
*Rex Ying, Ruining He, Kaifeng Chen, Pong Eksombatchai, William L. Hamilton, Jure Leskovec.* KDD 2018. [paper](https://arxiv.org/abs/1806.01973)

1. **Improved Semantic Representations From Tree-Structured Long Short-Term Memory Networks.**
*Kai Sheng Tai, Richard Socher, Christopher D. Manning.* ACL 2015. [paper](https://www.aclweb.org/anthology/P15-1150)

1. **Neural Module Networks.**
*Jacob Andreas, Marcus Rohrbach, Trevor Darrell, Dan Klein.* CVPR 2016. [paper](https://arxiv.org/pdf/1511.02799.pdf)

1. **Encoding Sentences with Graph Convolutional Networks for Semantic Role Labeling.**
*Diego Marcheggiani, Ivan Titov.* EMNLP 2017. [paper](https://arxiv.org/abs/1703.04826)

1. **Graph Convolutional Networks with Argument-Aware Pooling for Event Detection.**
*Thien Huu Nguyen, Ralph Grishman.* AAAI 2018. [paper](http://ix.cs.uoregon.edu/~thien/pubs/graphConv.pdf)

1. **Geometric Matrix Completion with Recurrent Multi-Graph Neural Networks.**
*Federico Monti, Michael M. Bronstein, Xavier Bresson.* NIPS 2017. [paper](https://arxiv.org/abs/1704.06803)

1. **Graph Convolutional Matrix Completion.**
*Rianne van den Berg, Thomas N. Kipf, Max Welling.* 2017. [paper](https://arxiv.org/abs/1706.02263)

1. **Hybrid Approach of Relation Network and Localized Graph Convolutional Filtering for Breast Cancer Subtype Classification.**
*Sungmin Rhee, Seokjun Seo, Sun Kim.* IJCAI 2018. [paper](https://arxiv.org/abs/1711.05859)

1. **Modeling polypharmacy side effects with graph convolutional networks.**
*Marinka Zitnik, Monica Agrawal, Jure Leskovec.* ISMB 2018. [paper](https://arxiv.org/abs/1802.00543)

1. **DeepInf: Modeling influence locality in large social networks.**
*Jiezhong Qiu, Jian Tang, Hao Ma, Yuxiao Dong, Kuansan Wang, Jie Tang.* KDD 2018. [paper](https://arxiv.org/pdf/1807.05560.pdf)

1. **Exploiting Semantics in Neural Machine Translation with Graph Convolutional Networks.**
*Diego Marcheggiani, Joost Bastings, Ivan Titov.* NAACL 2018. [paper](http://www.aclweb.org/anthology/N18-2078)

1. **Exploring Graph-structured Passage Representation for Multi-hop Reading Comprehension with Graph Neural Networks.**
*Linfeng Song, Zhiguo Wang, Mo Yu, Yue Zhang, Radu Florian, Daniel Gildea.* 2018. [paper](https://arxiv.org/abs/1809.02040)

1. **Graph Convolution over Pruned Dependency Trees Improves Relation Extraction.**
*Yuhao Zhang, Peng Qi, Christopher D. Manning.* EMNLP 2018. [paper](https://arxiv.org/abs/1809.10185)

1. **N-ary relation extraction using graph state LSTM.**
*Linfeng Song, Yue Zhang, Zhiguo Wang, Daniel Gildea.* EMNLP 18. [paper](https://arxiv.org/abs/1808.09101)

1. **A Graph-to-Sequence Model for AMR-to-Text Generation.**
*Linfeng Song, Yue Zhang, Zhiguo Wang, Daniel Gildea.* ACL 2018. [paper](https://arxiv.org/abs/1805.02473)

1. **Cross-Sentence N-ary Relation Extraction with Graph LSTMs.**
*Nanyun Peng, Hoifung Poon, Chris Quirk, Kristina Toutanova, Wen-tau Yih.* TACL. [paper](https://arxiv.org/abs/1708.03743)

1. **Sentence-State LSTM for Text Representation.**
*Yue Zhang, Qi Liu, Linfeng Song.*  ACL 2018. [paper](https://arxiv.org/abs/1805.02474)

1. **End-to-End Relation Extraction using LSTMs on Sequences and Tree Structures.**
*Makoto Miwa, Mohit Bansal.* ACL 2016. [paper](https://arxiv.org/abs/1601.00770)

1. **Learning Human-Object Interactions by Graph Parsing Neural Networks.**
*Siyuan Qi, Wenguan Wang, Baoxiong Jia, Jianbing Shen, Song-Chun Zhu.* ECCV 2018. [paper](https://arxiv.org/pdf/1808.07962.pdf)
