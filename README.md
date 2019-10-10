* 数据集：[GCN使用的数据集Cora、Citeseer、Pubmed、Tox21格式](https://blog.csdn.net/yyl424525/article/details/100831452)
> Cora数据集分为6大类，36个小类。主要的文件目录包括：
（1）papers：以<id> <filename> <citation string>的形式描述论文信息，其中citation string是该论文的任意一篇参考引文或者基于作者名和文章名提取出的关键字。
（2）citations：大约有715000条引文信息，用<referring_id> <cited_id>形式描述论文之间的引用关系。
（3）citations.withauthors：包含论文的引文信息和作者信息，描述格式为：<this_paper_id><filename><id_of_first_cited_paper><id_of_second_cited_paper>…<Author#1>(of this paper)<Author#2>…（4）classifications：记录论文的分类信息，但分类标签并不是很准确，其描述格式为：<filename> <classification>。如：http:##www.ri.cmu.edu#afs#cs#user#alex#docs#idvl#dl97.ps    /Information_Retrieval/Retrieval/。

* 论文笔记：[菜鸟笔记之《Large-Scale Learnable Graph Convolutional Networks》](https://www.jianshu.com/p/ada8730913ce)
* 论文原文：https://arxiv.org/pdf/1808.03965.pdf

---
# Large-Scale Learnable Graph Convolutional Networks(LGCN)

Created by [Hongyang Gao](http://eecs.wsu.edu/~hgao/), [Zhengyang Wang](http://www.eecs.wsu.edu/~zwang6/) and [Shuiwang Ji](http://www.eecs.wsu.edu/~sji/) at Washington State University.

Accepted by KDD18.

## Introduction

Large-Scale Learnable Graph Convolutional Networks provide an efficient way (LGCL and LGCN) for learnable graph convolution.

Detailed information about LGCL and LGCN is provided in (https://dl.acm.org/citation.cfm?id=3219947).

## Citation

If using this code, please cite our paper.

```
@inproceedings{gao2018large,
  title={Large-Scale Learnable Graph Convolutional Networks},
  author={Gao, Hongyang and Wang, Zhengyang and Ji, Shuiwang},
  booktitle={Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery \& Data Mining},
  pages={1416--1424},
  year={2018},
  organization={ACM}
}
```

## Start training

After configure the network, we can start to train. Run
```
python main.py
```
The training results on Cora dataset will be displayed.


## Results

| Models    | Cora  | Citeseer | Pubmed |
|-----------|-------|----------|--------|
| DeepWalk  | 67.2% | 43.2%    | 65.3%  |
| Planetoid | 75.7% | 64.7%    | 77.2%  |
| Chebyshev | 81.2% | 69.8%    | 74.4%  |
| GCN       | 81.5% | 70.3%    | 79.0%  |
| LGCN      |83.3 ± 0.5% | 73.0 ± 0.6% | 79.5 ± 0.2% |
