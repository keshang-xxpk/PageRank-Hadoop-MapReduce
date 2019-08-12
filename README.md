# PageRank project
## Introduction
In this project,I mock PageRank algorithm to rank websites in their search engine results using Hadoop,Mapreduce framework,Hbase,HDFS and etc.
## What is PageRank?
- PageRank is an algorithm used by Google Search to rank websites in
their search engine results.
- Paper from Google: http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=B12F2305C6BE51FF998B2024CFE71F05?doi=10.1.1.38.5427&rep=rep1&type=pdf
## Basic Theory behind PageRank
- Account Assumption：More important websites are likely to receive more links from other websites.
- Quantity Assumption:：Website with higher PageRank will pass higher weight.
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/PageRank.png)
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/PR.png)
- More important websites are likely to receive more links from otherwebsites.
    - Represent the directivity between pages:We use Transition Martrix.![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/transition%20matrix.png)
    -  Represent the importance of each website:We use PageRank Matrix.![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/PR%20Matrix.png)
- Calculate PR1:![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/how%20to%20caculate%20PR1.png)
