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
*  12/2020: 4
*  11/2020: 6
*  10/2020: 9
*  9/2020: 23
*  8/2020: 6
*  7/2020: 26
*  6/2020: 8
*  5/2020: 19
*  4/2020: 3
*  3/2020: 11
*  2/2020: 13
*  1/2020: 15

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

Total Matches: 74

Total Results (Limited by GitHUB API): 37

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [ipld/go-ipld-graphql](https://github.com/ipld/go-ipld-graphql)| 0 | 0 | 15| 2020-12-07 | 2020-12-18 |
| [ur-the-zissou/go-accumulator-dag](https://github.com/ur-the-zissou/go-accumulator-dag)| 3 | 0 | 23| 2020-11-08 | 2020-11-08 |
| [vulcanize/ipld-btc-server](https://github.com/vulcanize/ipld-btc-server)| 0 | 0 | 60230| 2020-08-26 | 2020-09-02 |
| [vulcanize/ipld-eth-server](https://github.com/vulcanize/ipld-eth-server)| 0 | 1 | 60517| 2020-08-26 | 2020-11-13 |
| [amirylm/libp2p-facade](https://github.com/amirylm/libp2p-facade)| 2 | 0 | 122| 2020-08-24 | 2020-11-28 |
| [vulcanize/ipld-btc-indexer](https://github.com/vulcanize/ipld-btc-indexer)| 0 | 0 | 60308| 2020-08-10 | 2020-09-10 |
| [dgtony/cidec](https://github.com/dgtony/cidec)| 0 | 0 | 7| 2020-06-24 | 2020-06-24 |
| [vulcanize/ipld-eth-indexer](https://github.com/vulcanize/ipld-eth-indexer)| 5 | 4 | 60415| 2020-05-27 | 2020-11-01 |
| [creationix/sel-parse-go](https://github.com/creationix/sel-parse-go)| 0 | 0 | 5| 2020-05-07 | 2020-05-17 |
| [jhamPac/purple](https://github.com/jhamPac/purple)| 0 | 0 | 4| 2020-04-19 | 2020-04-20 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 156

Total Results (Limited by GitHUB API): 78

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [rvagg/js-ipld-garbage](https://github.com/rvagg/js-ipld-garbage)| 0 | 0 | 13| 2020-12-17 | 2020-12-18 |
| [mikeal/fast-block-store](https://github.com/mikeal/fast-block-store)| 2 | 0 | 20| 2020-10-28 | 2020-10-29 |
| [rvagg/car-to-schema](https://github.com/rvagg/car-to-schema)| 0 | 1 | 14| 2020-10-24 | 2020-10-28 |
| [rvagg/js-ipld-schema-validator](https://github.com/rvagg/js-ipld-schema-validator)| 0 | 0 | 39| 2020-10-24 | 2020-11-20 |
| [rvagg/js-ipld-schema-describer](https://github.com/rvagg/js-ipld-schema-describer)| 1 | 0 | 14| 2020-10-21 | 2020-10-24 |
| [mikeal/simple-ipld-examples](https://github.com/mikeal/simple-ipld-examples)| 3 | 0 | 1| 2020-10-20 | 2020-10-20 |
| [mikeal/hamt-utils](https://github.com/mikeal/hamt-utils)| 0 | 0 | 10| 2020-09-10 | 2020-10-10 |
| [ipld/js-dag-pb](https://github.com/ipld/js-dag-pb)| 2 | 0 | 86876| 2020-09-02 | 2020-10-20 |
| [mikeal/lfs-store](https://github.com/mikeal/lfs-store)| 2 | 0 | 14| 2020-08-06 | 2020-09-09 |
| [keyko-io/filecoin-verifier-tools](https://github.com/keyko-io/filecoin-verifier-tools)| 2 | 1 | 886| 2020-07-15 | 2020-12-07 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
