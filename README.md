# PageRank project
## Introduction
In this project,I mock PageRank algorithm to rank websites in their search engine results using Hadoop,Mapreduce framework,Hbase,HDFS and etc.
## PageRank workflow
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/PR%20WORKFLOW.png)
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
- Calculate PR2:PR2=Transition Matrix * PR1
- Calculate PR(N):PR(N)=Transition Matrix * PR(N - 1)
## Implement PageRank with MapReduce
- Input format
        - Input1:Relations.txt
        - Input2:PR.txt 
- Implement PageRank with MapReduce
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/PR%20ON%20MR.png)
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/Screen%20Shot%202019-08-12%20at%202.39.37%20PM.png)
- MR1.Mapper1
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/MR1.Mapper1.png)
- MR1.Mapper2
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/MR2.Mapper2.png)
- MR1.Reducer
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/MR1.Reducer.png)
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/MR1.png)
- MR2.Mapper:Read file generated from last MR
- MR2.Reducer
![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/MR2.Reducer.png)

## Improvement
- There could be some edge cases:
        - Dead ends:PR(N) matrix will become zeros finally.
        - Spider traps:PR(N) matrix will be dominated by one page.
- Solution:![](https://github.com/keshang-xxpk/PageRank-Hadoop-MapReduce/blob/master/assert/improvement.png)
## Visualize PageRank Project
```BASH
#Download frontend source code 
wget https://s3-us-west-2.amazonaws.com/jiuzhang-bigdata/pagerank_search.tar
#Decompression the package
tar -xvf pagerank_search.tar
cd pagerank_search</pre>
```

