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
*  8/2021: 11
*  7/2021: 13
*  6/2021: 13
*  5/2021: 13
*  4/2021: 20
*  3/2021: 6
*  2/2021: 0
*  1/2021: 10
*  12/2020: 0
*  11/2020: 19
*  10/2020: 13
*  9/2020: 9

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

Total Matches: 94

Total Results (Limited by GitHUB API): 47

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [willscott/wasm-adl](https://github.com/willscott/wasm-adl)| 2 | 0 | 34| 2021-08-11 | 2021-08-13 |
| [simplecoincom/boltdb-to-ipld-hamt](https://github.com/simplecoincom/boltdb-to-ipld-hamt)| 0 | 0 | 9| 2021-08-04 | 2021-08-10 |
| [ipld/codec-fixtures](https://github.com/ipld/codec-fixtures)| 3 | 1 | 284| 2021-08-04 | 2021-08-27 |
| [simplecoincom/go-ipld-adl-hamt-container](https://github.com/simplecoincom/go-ipld-adl-hamt-container)| 0 | 0 | 147| 2021-07-29 | 2021-08-10 |
| [filecoin-project/dagstore](https://github.com/filecoin-project/dagstore)| 13 | 2 | 816| 2021-06-15 | 2021-08-24 |
| [daotl/go-ipld-channel](https://github.com/daotl/go-ipld-channel)| 0 | 0 | 19| 2021-06-13 | 2021-06-14 |
| [vulcanize/ipld-cosmos-indexer](https://github.com/vulcanize/ipld-cosmos-indexer)| 0 | 0 | 14| 2021-03-30 | 2021-03-30 |
| [ipfs/go-unixfsnode](https://github.com/ipfs/go-unixfsnode)| 1 | 2 | 152| 2021-03-05 | 2021-08-17 |
| [ipfs/go-fetcher](https://github.com/ipfs/go-fetcher)| 5 | 5 | 385| 2021-02-22 | 2021-08-18 |
| [ipfs/go-ipld-legacy](https://github.com/ipfs/go-ipld-legacy)| 2 | 0 | 39| 2021-02-12 | 2021-08-18 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 174

Total Results (Limited by GitHUB API): 87

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [maksympogonets/ultimate-ipfs-series](https://github.com/maksympogonets/ultimate-ipfs-series)| 2 | 0 | 47| 2021-08-30 | 2021-08-30 |
| [jimpick/js-car-zero-length-blocks](https://github.com/jimpick/js-car-zero-length-blocks)| 0 | 0 | 6| 2021-08-06 | 2021-08-06 |
| [ipld/js-ipld-format-to-blockcodec](https://github.com/ipld/js-ipld-format-to-blockcodec)| 0 | 0 | 85| 2021-07-28 | 2021-07-28 |
| [ipfs-examples/js-ipfs-traverse-ipld-grap...](https://github.com/ipfs-examples/js-ipfs-traverse-ipld-graphs)| 0 | 0 | 66| 2021-06-14 | 2021-08-24 |
| [ipfs-examples/js-ipfs-custom-ipld-format...](https://github.com/ipfs-examples/js-ipfs-custom-ipld-formats)| 0 | 0 | 23| 2021-06-14 | 2021-08-24 |
| [Electronic-Signatures-Industries/swarm-b...](https://github.com/Electronic-Signatures-Industries/swarm-bee-block-service)| 0 | 0 | 217| 2021-05-12 | 2021-05-12 |
| [ipld/js-blockcodec-to-ipld-format](https://github.com/ipld/js-blockcodec-to-ipld-format)| 0 | 1 | 106| 2021-04-30 | 2021-07-28 |
| [mikeal/encrypted-block](https://github.com/mikeal/encrypted-block)| 1 | 0 | 5| 2021-01-09 | 2021-01-09 |
| [mikeal/dag-query](https://github.com/mikeal/dag-query)| 0 | 0 | 4| 2021-01-02 | 2021-01-03 |
| [rvagg/js-ipld-garbage](https://github.com/rvagg/js-ipld-garbage)| 0 | 0 | 157| 2020-12-17 | 2021-08-05 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
