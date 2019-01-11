# Set Similarity Search Bencmarks

Benchmark data sets for set similarity search algorithms.

| Data set | Number of sets | Number of tokens | File size | Papers |
|----------|----------------|------------------|-----------|--------|
| [Canada-US-UK Open Data][od]<br/>[Query Benchmark 1k][od-1k]<br/>[Query Benchmark 10k][od-10k]<br/>[Query Benchmark 100k][od-100k] | 745,414 | 562,320,456 | 2.52 GB | (1) |
| [WDC Web Table 2015, English Relational-Only][webtable]<br/>[Query Benchmark 100][webtable-100]<br/>[Query Benchmark 1k][webtable-1k]<br/>[Query Benchmark 10k][webtable-10k] | 163,510,917 | 184,644,583 | 4.32 GB | (1,2) |

All data sets follow the same format:
* Compressed using gzip.
* First line of the main file is `<number of sets> <number of tokens>`.
* All other lines are `<set size>\t<1>,<2>,<3>,...`, where `\t` is a tab separator, `<1>` and so on are tokens.
* All tokens are integers, transformed from the original strings using a global ascending frequency order.

Papers in set similarity search using the above data sets:

1. [JOSIE: Overlap Set Similarity Search for Finding Joinable Tables in Data Lakes](), SIGMOD 2019 (To Appear)
2. [LSH Ensemble: Internet Scale Domain Search](http://www.vldb.org/pvldb/vol9/p1185-zhu.pdf), VLDB 2016

[od]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata.inp.gz
[od-1k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_1k.inp.gz
[od-10k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_10k.inp.gz
[od-100k]: https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata_queries_100k.inp.gz
[webtable]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational.inp.gz
[webtable-100]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_100.inp.gz
[webtable-1k]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_1k.inp.gz
[webtable-10k]: https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational_queries_10k.inp.gz
