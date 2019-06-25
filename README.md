# Ad Hoc Table Retrieval using Semantic Similarity

This repository contains resources developed within the following paper:

> S. Zhang and K. Balog. Ad Hoc Table Retrieval using Semantic Similarity. In: *Proceedings of the Web Conference 2018 (WWW '18)*, April 2018.


## Test collection

The table corpus is [WikiTables](http://websail-fe.cs.northwestern.edu/TabEL/), which comprises 1.6M tables extracted from Wikipedia. We proproceeed it and make it public downloadable [here](http://iai.group/downloads/smart_table/WP_tables.zip).

The `data/queries.txt` file contains the search queries. Queries #1-#30 queries constitute *Query subset 1 (QS-1)*, queries #31-#60 constitute *Query subset 2 (QS-2)*.

The `data/qrels.txt` file contains the relevance assessments (in TREC qrels format).  

## Data

We utilize word2vec trained on Google news, and you can find it [here](https://github.com/mmihaltz/word2vec-GoogleNews-vectors). You can find the graph embeddings [here](http://data.dws.informatik.uni-mannheim.de/rdf2vec/).



## Methods and results

The `rankings/` folder contains the table rankings generated by the various methods (in TREC runfile format).

|Method	|Runfile|	NDCG@5|	NDCG@10|	NDCG@15|	NDCG@20|
| -- | -- | -- | -- | -- | -- |
|Single-field document ranking | single_field.txt|	0.4770	|0.4860|	0.5170|	0.5473|
|Multi-field document ranking	|multi_field.txt|	0.4344|	0.4586|	0.4924|	0.5254|
|WebTable|	WebTable.txt        |	0.2831|	0.2992	|0.3311	|0.3726|
|WikiTable|	WikiTable.txt       |	0.4903	|0.4766|	0.5062	|0.5206|
|LTR|	LTR.txt|	0.5527|	0.5456|	0.5738	|0.6031|
|STR|	STR.txt|	0.5951|	0.6293|	0.6590|	0.6825|







The evaluation scores are reported using [trec_eval](https://github.com/usnistgov/trec_eval).


## Citation
```
@inproceedings{Zhang:2018:AHT,
    author = {Zhang, Shuo and Balog, Krisztian},
    title = {Ad Hoc Table Retrieval using Semantic Similarity},
    booktitle = {Proceedings of the Web Conference 2018},
    year = {2018},
    pages = {1553--1562},
}
```

## Contact
If you have any questions, please contact Shuo Zhang at shuo.zhang@uis.no.
