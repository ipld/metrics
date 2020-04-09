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
*  4/2020: 0
*  3/2020: 15
*  2/2020: 24
*  1/2020: 13
*  12/2019: 7
*  11/2019: 7
*  10/2019: 17
*  9/2019: 0
*  8/2019: 7
*  7/2019: 14
*  6/2019: 0
*  5/2019: 18

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

Total Matches: 54

Total Results (Limited by GitHUB API): 27

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [cuitaixiang/go-ipld-prime-notes](https://github.com/cuitaixiang/go-ipld-prime-notes)| 0 | 0 | 858| 2020-04-08 | 2020-04-08 |
| [jameshih/ipld-bookstore](https://github.com/jameshih/ipld-bookstore)| 0 | 0 | 8| 2020-02-04 | 2020-02-05 |
| [likecoin/iscn-ipld](https://github.com/likecoin/iscn-ipld)| 0 | 0 | 46| 2020-02-03 | 2020-03-02 |
| [likecoin/iscn-poc](https://github.com/likecoin/iscn-poc)| 0 | 0 | 74| 2020-01-30 | 2020-03-02 |
| [rvagg/go-car-example](https://github.com/rvagg/go-car-example)| 0 | 0 | 16| 2019-12-05 | 2019-12-06 |
| [0zAND1z/redis-ipld-benchmark](https://github.com/0zAND1z/redis-ipld-benchmark)| 0 | 0 | 5| 2019-12-05 | 2019-12-08 |
| [ipld/go-ipld-prime-proto](https://github.com/ipld/go-ipld-prime-proto)| 0 | 0 | 90| 2019-10-25 | 2020-03-31 |
| [0zAND1z/ipld-crud](https://github.com/0zAND1z/ipld-crud)| 5 | 0 | 31| 2019-10-24 | 2020-01-15 |
| [filecoin-project/go-amt-ipld](https://github.com/filecoin-project/go-amt-ipld)| 1 | 2 | 61| 2019-08-28 | 2020-04-06 |
| [rvagg/go-datastore-zipcar](https://github.com/rvagg/go-datastore-zipcar)| 2 | 0 | 57| 2019-08-06 | 2019-08-13 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 144

Total Results (Limited by GitHUB API): 72

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [chafey/ipld-schema-app](https://github.com/chafey/ipld-schema-app)| 1 | 0 | 1792| 2020-03-20 | 2020-03-25 |
| [rvagg/js-example-dag-generate](https://github.com/rvagg/js-example-dag-generate)| 0 | 0 | 2| 2020-03-18 | 2020-03-18 |
| [chafey/js-ipld-blockstore](https://github.com/chafey/js-ipld-blockstore)| 0 | 0 | 5| 2020-02-28 | 2020-02-29 |
| [ipld/js-schema-validation](https://github.com/ipld/js-schema-validation)| 0 | 0 | 29| 2020-02-27 | 2020-04-01 |
| [mikeal/dagdb](https://github.com/mikeal/dagdb)| 13 | 2 | 720| 2020-02-13 | 2020-04-08 |
| [mikeal/export-ipld-graph](https://github.com/mikeal/export-ipld-graph)| 1 | 0 | 1| 2020-02-05 | 2020-02-05 |
| [mikeal/s3-block-store](https://github.com/mikeal/s3-block-store)| 2 | 0 | 2| 2019-12-10 | 2019-12-10 |
| [rvagg/js-ipld-vector](https://github.com/rvagg/js-ipld-vector)| 1 | 0 | 20| 2019-12-09 | 2019-12-09 |
| [mikeal/csv-ipld-schema-gen](https://github.com/mikeal/csv-ipld-schema-gen)| 0 | 0 | 8| 2019-11-27 | 2019-12-03 |
| [simpleaswater/ipld](https://github.com/simpleaswater/ipld)| 1 | 0 | 58| 2019-10-05 | 2020-04-03 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
