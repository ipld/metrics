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
*  6/2021: 12
*  5/2021: 9
*  4/2021: 0
*  3/2021: 6
*  2/2021: 7
*  1/2021: 6
*  12/2020: 6
*  11/2020: 3
*  10/2020: 12
*  9/2020: 9
*  8/2020: 0
*  7/2020: 14

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
| [ipfs/go-unixfsnode](https://github.com/ipfs/go-unixfsnode)| 1 | 0 | 114| 2021-03-05 | 2021-06-01 |
| [ipfs/go-fetcher](https://github.com/ipfs/go-fetcher)| 4 | 3 | 315| 2021-02-22 | 2021-06-01 |
| [ipfs/go-ipld-legacy](https://github.com/ipfs/go-ipld-legacy)| 1 | 0 | 29| 2021-02-12 | 2021-06-01 |
| [ipld/go-ipld-graphql](https://github.com/ipld/go-ipld-graphql)| 4 | 2 | 81| 2020-12-07 | 2021-06-08 |
| [ur-the-zissou/go-accumulator-dag](https://github.com/ur-the-zissou/go-accumulator-dag)| 3 | 0 | 23| 2020-11-08 | 2020-11-08 |
| [vulcanize/ipld-btc-server](https://github.com/vulcanize/ipld-btc-server)| 0 | 0 | 60230| 2020-08-26 | 2020-09-02 |
| [vulcanize/ipld-eth-server](https://github.com/vulcanize/ipld-eth-server)| 1 | 2 | 61157| 2020-08-26 | 2021-06-10 |
| [amirylm/libp2p-facade](https://github.com/amirylm/libp2p-facade)| 3 | 0 | 157| 2020-08-24 | 2021-05-22 |
| [vulcanize/ipld-btc-indexer](https://github.com/vulcanize/ipld-btc-indexer)| 0 | 0 | 60308| 2020-08-10 | 2020-09-10 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 168

Total Results (Limited by GitHUB API): 84

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [oliveriosousa/js-ipfs-example-custom-tra...](https://github.com/oliveriosousa/js-ipfs-example-custom-traverse-ipld-graphs)| 0 | 0 | 50| 2021-06-07 | 2021-06-07 |
| [oliveriosousa/js-ipfs-example-custom-ipl...](https://github.com/oliveriosousa/js-ipfs-example-custom-ipld-formats)| 0 | 0 | 10| 2021-06-07 | 2021-06-07 |
| [Electronic-Signatures-Industries/swarm-b...](https://github.com/Electronic-Signatures-Industries/swarm-bee-block-service)| 0 | 0 | 217| 2021-05-12 | 2021-05-12 |
| [ipld/js-blockcodec-to-ipld-format](https://github.com/ipld/js-blockcodec-to-ipld-format)| 0 | 1 | 100| 2021-04-30 | 2021-05-06 |
| [mikeal/encrypted-block](https://github.com/mikeal/encrypted-block)| 1 | 0 | 5| 2021-01-09 | 2021-01-09 |
| [mikeal/dag-query](https://github.com/mikeal/dag-query)| 0 | 0 | 4| 2021-01-02 | 2021-01-03 |
| [rvagg/js-ipld-garbage](https://github.com/rvagg/js-ipld-garbage)| 0 | 0 | 143| 2020-12-17 | 2021-05-27 |
| [mikeal/fast-block-store](https://github.com/mikeal/fast-block-store)| 2 | 0 | 20| 2020-10-28 | 2020-10-29 |
| [rvagg/car-to-schema](https://github.com/rvagg/car-to-schema)| 0 | 1 | 14| 2020-10-24 | 2020-10-28 |
| [rvagg/js-ipld-schema-validator](https://github.com/rvagg/js-ipld-schema-validator)| 0 | 0 | 54| 2020-10-24 | 2021-06-12 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
