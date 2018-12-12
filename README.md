# Analysis on MSMARCO MRC Submissions

A list of analysis on the leaderboard, which focuses on the MRC task on MS-MARCO.

Contributed by Yuqiang Xie and Xing Luxi, National Engineering Laboratory for Information Security Technologies, Institute of Information Engineering, Chinese Academy of Sciences, Beijing, China.

## Introduction

[MS MARCO](https://arxiv.org/pdf/1611.09268.pdf) (Microsoft Machine Reading Comprehension) is a large scale dataset focused on machine reading comprehension, question answering, and passage ranking. The current dataset has 1,010,916 unique real queries that were generated by sampling and anonymizing Bing usage logs. For more details, see the project: [MSMARCOV2](https://github.com/dfcf93/MSMARCOV2).

**MSMARCO** is a benchmark dataset for multi-passage MRC or so-called "generative MRC". Besides, different from other MRC datasets, MSMARCO has the following advantages:

1. Real questions: All questions have been sample from real anonymized bing queries.
2. Real Documents: Most Url's that we have source the passages from contain the full web documents. These can be used as extra contextual information to improve systems or be used to compete in our expert task.
3. Human Generated Answers: All questions have an answer written by a human. If there was no answer in the passages the judge read they have written 'No Answer Present.'
4. Human Generated Well-Formed: Some questions contain extra human evaluation to create well formed answers that could be used by intelligent agents like Cortana, Siri, Google Assistant, and Alexa.
5. Dataset Size: At over 1 million queries the dataset is large enough to train the most complex systems and also sample the data for specific applications.

In this repository, submissions to MSMARCO will be almostly listed.  This work will be updated persistently.

Tips: The official evaluation metrics include [ROUGE-L](http://aclweb.org/anthology/W04-1013) and [BLEU-1](http://www.anthology.aclweb.org/P/P02/P02-1040.pdf). 

## V1 Leaderboard - Model List

Task Definition: Given a question and a set of passages (top 10) retrieved
by search engines, the task is to find the best concise answer to the question. 

|Rank|Model| Org. | Rouge-L | Bleu-1 | Description |
|:----|:----|:-------|:-----:|:-----:|:----:|
|1|MARS| YUANFUDAO research NLP | 49.72| 48.02 | [link]() |
|2|Human Performance| -  |47.00| 46.00 |[link]() |
|3|[V-Net](https://arxiv.org/pdf/1805.02220.pdf)| Baidu NLP | 46.15 | 44.46 |[link]() |
|4|[S-Net](https://arxiv.org/pdf/1706.04815.pdf)| Microsoft AI and Research |45.23| 43.78|[link]() |
|5|[R-Net](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/05/r-net.pdf)| Microsoft AI and Research |42.89| 42.22|[link]() |
|6|[ReasoNet](https://arxiv.org/pdf/1609.05284.pdf)| Microsoft AI and Research |38.81| 39.86|[link]() |
|7|[Prediction](https://arxiv.org/abs/1608.07905.pdf)| Singapore Management University |37.67| 33.93|[link]() |
|8|[FastQA_Ext](https://arxiv.org/pdf/1703.04816.pdf)| DFKI German Research Center for AI |33.67| 33.93|[link]() |


## V2 Leaderboard - Model List

For this version, we focus on *Q&A + Natural Langauge Generation*, where human performance is 63.21 on Rouge-L.

Task Definition: Given a query and 10 passages provide the best answer avaible in natural languauge that could be used by a smart device/digital assistant.

|Rank| Model      | Org.  | Rouge-L | Bleu-1 |
| :--------- | :---- | :----------- | :--------- | :-------- |
|1| Human Performance    | -   |      63.21        |   53.03  |
|2| V-Net  | Baidu NLP |  48.37		 | 46.75 |
|3| Masque | NTT Media Intelligence Laboratories| 46.81 |47.64 |
|4| SNET + CES2S   | SYSU     |    45.04          |  40.62  |
|5| Reader-Writer   |  Microsoft Business Applications Group AI Research     |    43.89          |    42.59        |
|6| ConZNet |   Samsung Research    |    42.14          | 38.62 |
