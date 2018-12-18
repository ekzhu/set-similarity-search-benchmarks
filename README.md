# Set Similarity Search Bencmarks

Benchmark data sets for set similarity search algorithms.

| Data set | Number of sets | Number of tokens | File size | Papers |
|----------|----------------|------------------|-----------|--------|
| [Canada-US-UK Open Data](https://storage.googleapis.com/set-similarity-search/canada_us_uk_opendata.inp.gz) | 745,414 | 562,320,456 | 2.52 GB | [1] |
| [WDC Web Table 2015, English Relational-Only](https://storage.googleapis.com/set-similarity-search/wdc_webtables_2015_english_relational.inp.gz) | 163,510,917 | 184,644,583 | 4.32 GB | [1,2] |

All data sets follow the same format:
* First line is `<number of sets> <number of tokens>`.
* All other lines are `<set size>\t<1>,<2>,<3>,...`, where `\t` is a tab separator, `<1>` and so on are tokens.
* All tokens are integers, transformed from the original strings using a global ascending frequency order.

Papers in set similarity search using the above data sets:

1. A Set Overlap Search Algorithm for Finding Joinable Tables in Massive Data Lakes, SIGMOD 2019 (To Appear)
2. [LSH Ensemble: Internet Scale Domain Search](http://www.vldb.org/pvldb/vol9/p1185-zhu.pdf), VLDB 2016
