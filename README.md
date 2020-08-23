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
*  8/2020: 7
*  7/2020: 11
*  6/2020: 11
*  5/2020: 5
*  4/2020: 7
*  3/2020: 3
*  2/2020: 16
*  1/2020: 11
*  12/2019: 5
*  11/2019: 5
*  10/2019: 11
*  9/2019: 6

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

Total Matches: 60

Total Results (Limited by GitHUB API): 30

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [dgtony/cidec](https://github.com/dgtony/cidec)| 0 | 0 | 7| 2020-06-24 | 2020-06-24 |
| [creationix/sel-parse-go](https://github.com/creationix/sel-parse-go)| 0 | 0 | 5| 2020-05-07 | 2020-05-17 |
| [jhamPac/purple](https://github.com/jhamPac/purple)| 0 | 0 | 4| 2020-04-19 | 2020-04-20 |
| [cuitaixiang/go-ipld-prime-notes](https://github.com/cuitaixiang/go-ipld-prime-notes)| 0 | 0 | 867| 2020-04-08 | 2020-04-14 |
| [jameshih/ipld-bookstore](https://github.com/jameshih/ipld-bookstore)| 0 | 0 | 8| 2020-02-04 | 2020-02-05 |
| [likecoin/iscn-ipld](https://github.com/likecoin/iscn-ipld)| 1 | 1 | 128| 2020-02-03 | 2020-05-17 |
| [likecoin/iscn-poc](https://github.com/likecoin/iscn-poc)| 1 | 1 | 179| 2020-01-30 | 2020-05-16 |
| [rvagg/go-car-example](https://github.com/rvagg/go-car-example)| 0 | 1 | 16| 2019-12-05 | 2019-12-06 |
| [0zAND1z/redis-ipld-benchmark](https://github.com/0zAND1z/redis-ipld-benchmark)| 0 | 0 | 5| 2019-12-05 | 2019-12-08 |
| [ipld/go-ipld-prime-proto](https://github.com/ipld/go-ipld-prime-proto)| 0 | 2 | 108| 2019-10-25 | 2020-04-28 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 140

Total Results (Limited by GitHUB API): 70

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [mikeal/lfs-store](https://github.com/mikeal/lfs-store)| 1 | 0 | 7| 2020-08-06 | 2020-08-07 |
| [keyko-io/filecoin-verifier-tools](https://github.com/keyko-io/filecoin-verifier-tools)| 1 | 1 | 158| 2020-07-15 | 2020-08-21 |
| [ipld/docs](https://github.com/ipld/docs)| 2 | 0 | 1472| 2020-07-10 | 2020-07-29 |
| [rvagg/js-zcash](https://github.com/rvagg/js-zcash)| 1 | 0 | 51| 2020-06-29 | 2020-06-29 |
| [ipld/js-bitcoin](https://github.com/ipld/js-bitcoin)| 0 | 0 | 15881| 2020-05-27 | 2020-06-29 |
| [ipld/js-dag-cbor](https://github.com/ipld/js-dag-cbor)| 1 | 0 | 199| 2020-05-12 | 2020-08-20 |
| [chafey/ipld-schema-app](https://github.com/chafey/ipld-schema-app)| 1 | 0 | 2329| 2020-03-20 | 2020-08-08 |
| [rvagg/js-example-dag-generate](https://github.com/rvagg/js-example-dag-generate)| 0 | 0 | 2| 2020-03-18 | 2020-03-18 |
| [chafey/js-ipld-blockstore](https://github.com/chafey/js-ipld-blockstore)| 0 | 0 | 5| 2020-02-28 | 2020-02-29 |
| [ipld/js-schema-validation](https://github.com/ipld/js-schema-validation)| 0 | 0 | 52| 2020-02-27 | 2020-08-20 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
