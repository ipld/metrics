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
*  5/2021: 4
*  4/2021: 10
*  3/2021: 9
*  2/2021: 3
*  1/2021: 7
*  12/2020: 2
*  11/2020: 7
*  10/2020: 5
*  9/2020: 16
*  8/2020: 5
*  7/2020: 14
*  6/2020: 7

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

Total Matches: 82

Total Results (Limited by GitHUB API): 41

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [vulcanize/ipld-cosmos-indexer](https://github.com/vulcanize/ipld-cosmos-indexer)| 0 | 0 | 14| 2021-03-30 | 2021-03-30 |
| [ipfs/go-unixfsnode](https://github.com/ipfs/go-unixfsnode)| 1 | 0 | 114| 2021-03-05 | 2021-04-23 |
| [ipfs/go-fetcher](https://github.com/ipfs/go-fetcher)| 4 | 3 | 315| 2021-02-22 | 2021-05-17 |
| [ipfs/go-ipld-legacy](https://github.com/ipfs/go-ipld-legacy)| 1 | 0 | 27| 2021-02-12 | 2021-04-23 |
| [ipld/go-ipld-graphql](https://github.com/ipld/go-ipld-graphql)| 4 | 2 | 68| 2020-12-07 | 2021-04-25 |
| [ur-the-zissou/go-accumulator-dag](https://github.com/ur-the-zissou/go-accumulator-dag)| 3 | 0 | 23| 2020-11-08 | 2020-11-08 |
| [vulcanize/ipld-btc-server](https://github.com/vulcanize/ipld-btc-server)| 0 | 0 | 60230| 2020-08-26 | 2020-09-02 |
| [vulcanize/ipld-eth-server](https://github.com/vulcanize/ipld-eth-server)| 1 | 1 | 61088| 2020-08-26 | 2021-04-29 |
| [amirylm/libp2p-facade](https://github.com/amirylm/libp2p-facade)| 3 | 0 | 157| 2020-08-24 | 2021-05-22 |
| [vulcanize/ipld-btc-indexer](https://github.com/vulcanize/ipld-btc-indexer)| 0 | 0 | 60308| 2020-08-10 | 2020-09-10 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 164

Total Results (Limited by GitHUB API): 82

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [Electronic-Signatures-Industries/swarm-b...](https://github.com/Electronic-Signatures-Industries/swarm-bee-block-service)| 0 | 0 | 217| 2021-05-12 | 2021-05-12 |
| [ipld/js-blockcodec-to-ipld-format](https://github.com/ipld/js-blockcodec-to-ipld-format)| 0 | 1 | 100| 2021-04-30 | 2021-05-06 |
| [mikeal/encrypted-block](https://github.com/mikeal/encrypted-block)| 1 | 0 | 5| 2021-01-09 | 2021-01-09 |
| [mikeal/dag-query](https://github.com/mikeal/dag-query)| 0 | 0 | 4| 2021-01-02 | 2021-01-03 |
| [rvagg/js-ipld-garbage](https://github.com/rvagg/js-ipld-garbage)| 0 | 0 | 34| 2020-12-17 | 2021-05-12 |
| [mikeal/fast-block-store](https://github.com/mikeal/fast-block-store)| 2 | 0 | 20| 2020-10-28 | 2020-10-29 |
| [rvagg/car-to-schema](https://github.com/rvagg/car-to-schema)| 0 | 1 | 14| 2020-10-24 | 2020-10-28 |
| [rvagg/js-ipld-schema-validator](https://github.com/rvagg/js-ipld-schema-validator)| 0 | 0 | 39| 2020-10-24 | 2020-11-20 |
| [rvagg/js-ipld-schema-describer](https://github.com/rvagg/js-ipld-schema-describer)| 2 | 0 | 14| 2020-10-21 | 2020-10-24 |
| [mikeal/simple-ipld-examples](https://github.com/mikeal/simple-ipld-examples)| 3 | 0 | 1| 2020-10-20 | 2020-10-20 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
