# metrics repo

Regularly collect and log metrics about IPLD related projects.

This repo contains a scheduled GitHub Action which pulls IPLD dependency data out of BigQuery and stores it 
in [timestamped json](./logs) files in this repo.

## Recent Data

### Google Trends

We're collecting the "interest over time" metric from Google Trends. From Google *"Numbers 
represent search interest relative to the highest point on the chart for the given region and 
time. A value of 100 is the peak popularity for the term. A value of 50 means that the term is 
half as popular. Likewise a score of 0 means the term was less than 1% as popular as the peak."*

This is the google trend data for searches of the term "IPLD" for the
last 12 months. The last 10 years is [available here.](./results/google-trends.md)



Google Trends:
*  2/2020: 15
*  1/2020: 10
*  12/2019: 5
*  11/2019: 7
*  10/2019: 7
*  9/2019: 7
*  8/2019: 10
*  7/2019: 5
*  6/2019: 7
*  5/2019: 9
*  4/2019: 12
*  3/2019: 8

### GitHub Search

These do a repository search, filtered by language, for "ipld." This search
finds references to ipld in project names, descriptions, and anything else
GitHub finds relevant (this isn't actually documented very well by GitHub).

GitHub limits the maximum results to 1K. We can get around this a little bit
by performing additional queries w/ different sorts in ascending and descending
order, but there's some amount we'll never get. That's why it's nice to have
the historical data logged in the repo every day.

The "total matches" we get is larger than the result set, even when the result
set is below the 1K limit imposed by GitHub. This isn't documented sufficiently
so we don't know why this is the case.

#### Go Repositories

Total Matches: 52

Total Results (Limited by GitHUB API): 26

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [jameshih/ipld-bookstore](https://github.com/jameshih/ipld-bookstore)| 0 | 0 | 8| 2020-02-04 | 2020-02-05 |
| [likecoin/likecoin-iscn-ipld](https://github.com/likecoin/likecoin-iscn-ipld)| 0 | 0 | 43| 2020-02-03 | 2020-02-21 |
| [likecoin/likecoin-iscn-poc](https://github.com/likecoin/likecoin-iscn-poc)| 0 | 0 | 72| 2020-01-30 | 2020-02-21 |
| [rvagg/go-car-example](https://github.com/rvagg/go-car-example)| 0 | 0 | 16| 2019-12-05 | 2019-12-06 |
| [0zAND1z/redis-ipld-benchmark](https://github.com/0zAND1z/redis-ipld-benchmark)| 0 | 0 | 5| 2019-12-05 | 2019-12-08 |
| [ipld/go-ipld-prime-proto](https://github.com/ipld/go-ipld-prime-proto)| 0 | 0 | 44| 2019-10-25 | 2019-11-13 |
| [0zAND1z/ipld-crud](https://github.com/0zAND1z/ipld-crud)| 5 | 0 | 31| 2019-10-24 | 2020-01-15 |
| [filecoin-project/go-amt-ipld](https://github.com/filecoin-project/go-amt-ipld)| 1 | 2 | 59| 2019-08-28 | 2020-01-31 |
| [rvagg/go-datastore-zipcar](https://github.com/rvagg/go-datastore-zipcar)| 2 | 0 | 57| 2019-08-06 | 2019-08-13 |
| [Netflix/p2plab](https://github.com/Netflix/p2plab)| 73 | 11 | 16688| 2019-07-27 | 2020-02-19 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 140

Total Results (Limited by GitHUB API): 70

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [chafey/js-ipld-blockstore](https://github.com/chafey/js-ipld-blockstore)| 0 | 0 | 5| 2020-02-28 | 2020-02-29 |
| [mikeal/ipld-schema-validation](https://github.com/mikeal/ipld-schema-validation)| 0 | 0 | 6| 2020-02-27 | 2020-02-27 |
| [mikeal/dagdb](https://github.com/mikeal/dagdb)| 7 | 0 | 39| 2020-02-13 | 2020-02-28 |
| [mikeal/export-ipld-graph](https://github.com/mikeal/export-ipld-graph)| 1 | 0 | 1| 2020-02-05 | 2020-02-05 |
| [mikeal/s3-block-store](https://github.com/mikeal/s3-block-store)| 2 | 0 | 2| 2019-12-10 | 2019-12-10 |
| [rvagg/js-ipld-vector](https://github.com/rvagg/js-ipld-vector)| 1 | 0 | 20| 2019-12-09 | 2019-12-09 |
| [mikeal/csv-ipld-schema-gen](https://github.com/mikeal/csv-ipld-schema-gen)| 0 | 0 | 8| 2019-11-27 | 2019-12-03 |
| [simpleaswater/ipld](https://github.com/simpleaswater/ipld)| 1 | 0 | 22| 2019-10-05 | 2020-01-15 |
| [rvagg/js-ipld-hashmap](https://github.com/rvagg/js-ipld-hashmap)| 7 | 0 | 19| 2019-08-26 | 2019-08-28 |
| [ipld/metrics](https://github.com/ipld/metrics)| 0 | 0 | 1243| 2019-08-25 | 2020-02-29 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
