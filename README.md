# Set Similarity Search Bencmarks

Benchmark data sets for set similarity search algorithms.

| Data set | Note |  Number of sets | Number of tokens | File size | Papers |
|----------|------|-----------------|------------------|-----------|--------|
| [BMS-POS][bms] ([Source](http://www.kdd.org/kdd-cup/view/kdd-cup-2000)) | A set is a purchase in a shop; a token is a product category in that purchase | 515,597 | 1,657 | 3.8 MB | 1 |
| [Kosarak][kosarak] ([Source](http://fimi.ua.ac.be/data)) | A set is a user; a token is a link clicked by the user | 990,002 | 41,270 | 13 MB | 1 |
| [Flickr][flickr] | A set is a photo; a token is a tag or a word from the title | 1,680,490 | 810,660 | 29 MB | 1,4 |
| [Netflix][netflix] ([Source](http://www.cs.uic.edu/∼liub/Netflix-KDD-Cup-2007.html)) | A set is a user; a token is a movie rated by the user | 480,189 | 17,770 | 166 MB | 1 |
| [Orkut][orkut] ([Source](http://socialnetworks.mpi-sws.org/data-imc2007.html)) | A set is a user; a token is a group membership of the user | 1,853,285 | 15,293,693 | 378 MB | 1 |
| [Canada-US-UK Open Data][od]<br/>[Query Benchmark 1k][od-1k]<br/>[Query Benchmark 10k][od-10k]<br/>[Query Benchmark 100k][od-100k] | A set is a table column; a token is a data value | 745,414 | 562,320,456 | 2.52 GB | 2 |
| [WDC Web Table 2015, English Relational-Only][webtable]<br/>[Query Benchmark 100][webtable-100]<br/>[Query Benchmark 1k][webtable-1k]<br/>[Query Benchmark 10k][webtable-10k] | A set is a table column; a token is a data value | 163,510,917 | 184,644,583 | 4.32 GB | 2,3 |

<!-- 
| [Flickr-LC][flickr-lc] - modified Flickr for small sets | 3,546,729 | 618,971 | 27 MB | (3,5) |
| [Twitter][twitter] - a data set partitioning the Twitter graph based on node neighborhood | 371,586 | 1,318 | 12 MB | (3,5) |
| [Webbase][webbase] - web pages with at least 200 hyperlinks taken from the [Stanford WebBase project](http://ilpubs.stanford.edu:8090/380/1/1999-26.pdf) | 168,707 | 15,146,263 | 118 MB | (3,5) | 
-->

All data sets follow the same format:
* Compressed using gzip.
* First line of the main file is `<number of sets> <number of tokens>`.
* All other lines are `<set size>\t<1>,<2>,<3>,...`, where `\t` is a tab separator, `<1>` and so on are tokens.
* All tokens are integers, transformed from the original strings using a global ascending frequency order.

Papers in set similarity search using the above data sets:

1. [An Empirical Evaluation of Set Similarity Join Techniques](http://www.vldb.org/pvldb/vol9/p636-mann.pdf), VLDB 2016
2. [LSH Ensemble: Internet Scale Domain Search](http://www.vldb.org/pvldb/vol9/p1185-zhu.pdf), VLDB 2016
3. [JOSIE: Overlap Set Similarity Search for Finding Joinable Tables in Data Lakes](), SIGMOD 2019 (To Appear)
4. [Spatio-textual similarity joins](http://www.vldb.org/pvldb/vol6/p1-bouros.pdf), VLDB 2012



[od]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata.inp.gz
[od-1k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_1k.inp.gz
[od-10k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_10k.inp.gz
[od-100k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_100k.inp.gz
[webtable]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational.inp.gz
[webtable-100]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_100.inp.gz
[webtable-1k]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_1k.inp.gz
[webtable-10k]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_10k.inp.gz
[bms]: https://storage.googleapis.com/set-similarity-search/BMS-POS_dup_dr.inp.gz
[flickr]: https://storage.googleapis.com/set-similarity-search/FLICKR-london2y_dup_dr.inp.gz
[flickr-lc]: https://storage.googleapis.com/set-similarity-search/flickr_set.inp.gz
[kosarak]: https://storage.googleapis.com/set-similarity-search/KOSARAK_dup_dr.inp.gz
[netflix]: https://storage.googleapis.com/set-similarity-search/NETFLIX_dup_dr.inp.gz
[orkut]: https://storage.googleapis.com/set-similarity-search/orkut_ge10.inp.gz
[twitter]: https://storage.googleapis.com/set-similarity-search/twitter_ge30.inp.gz
[webbase]: https://storage.googleapis.com/set-similarity-search/webbase_ge200.inp.gz
