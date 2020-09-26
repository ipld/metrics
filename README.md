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
*  9/2020: 8
*  8/2020: 7
*  7/2020: 10
*  6/2020: 4
*  5/2020: 8
*  4/2020: 3
*  3/2020: 6
*  2/2020: 11
*  1/2020: 7
*  12/2019: 4
*  11/2019: 4
*  10/2019: 4

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

Total Matches: 68

Total Results (Limited by GitHUB API): 34

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [vulcanize/ipld-btc-server](https://github.com/vulcanize/ipld-btc-server)| 0 | 0 | 60230| 2020-08-26 | 2020-09-02 |
| [vulcanize/ipld-eth-server](https://github.com/vulcanize/ipld-eth-server)| 0 | 0 | 60396| 2020-08-26 | 2020-09-25 |
| [vulcanize/ipld-btc-indexer](https://github.com/vulcanize/ipld-btc-indexer)| 0 | 0 | 60308| 2020-08-10 | 2020-09-10 |
| [dgtony/cidec](https://github.com/dgtony/cidec)| 0 | 0 | 7| 2020-06-24 | 2020-06-24 |
| [vulcanize/ipld-eth-indexer](https://github.com/vulcanize/ipld-eth-indexer)| 4 | 3 | 60251| 2020-05-27 | 2020-09-24 |
| [creationix/sel-parse-go](https://github.com/creationix/sel-parse-go)| 0 | 0 | 5| 2020-05-07 | 2020-05-17 |
| [jhamPac/purple](https://github.com/jhamPac/purple)| 0 | 0 | 4| 2020-04-19 | 2020-04-20 |
| [cuitaixiang/go-ipld-prime-notes](https://github.com/cuitaixiang/go-ipld-prime-notes)| 0 | 0 | 867| 2020-04-08 | 2020-04-14 |
| [jameshih/ipld-bookstore](https://github.com/jameshih/ipld-bookstore)| 0 | 0 | 8| 2020-02-04 | 2020-02-05 |
| [likecoin/iscn-ipld](https://github.com/likecoin/iscn-ipld)| 1 | 1 | 128| 2020-02-03 | 2020-05-17 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 144

Total Results (Limited by GitHUB API): 72

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [mikeal/hamt-utils](https://github.com/mikeal/hamt-utils)| 0 | 0 | 6| 2020-09-10 | 2020-09-11 |
| [ipld/js-dag-pb](https://github.com/ipld/js-dag-pb)| 2 | 0 | 86837| 2020-09-02 | 2020-09-24 |
| [mikeal/lfs-store](https://github.com/mikeal/lfs-store)| 1 | 0 | 14| 2020-08-06 | 2020-09-09 |
| [keyko-io/filecoin-verifier-tools](https://github.com/keyko-io/filecoin-verifier-tools)| 2 | 1 | 621| 2020-07-15 | 2020-09-25 |
| [ipld/docs](https://github.com/ipld/docs)| 3 | 1 | 1550| 2020-07-10 | 2020-09-18 |
| [rvagg/js-zcash](https://github.com/rvagg/js-zcash)| 1 | 0 | 52| 2020-06-29 | 2020-09-01 |
| [ipld/js-bitcoin](https://github.com/ipld/js-bitcoin)| 0 | 0 | 15883| 2020-05-27 | 2020-09-01 |
| [ipld/js-dag-cbor](https://github.com/ipld/js-dag-cbor)| 1 | 1 | 176| 2020-05-12 | 2020-09-16 |
| [chafey/ipld-schema-app](https://github.com/chafey/ipld-schema-app)| 1 | 0 | 2463| 2020-03-20 | 2020-09-11 |
| [rvagg/js-example-dag-generate](https://github.com/rvagg/js-example-dag-generate)| 0 | 0 | 2| 2020-03-18 | 2020-03-18 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
