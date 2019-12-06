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
*  12/2019: 0
*  11/2019: 14
*  10/2019: 14
*  9/2019: 5
*  8/2019: 12
*  7/2019: 20
*  6/2019: 17
*  5/2019: 21
*  4/2019: 21
*  3/2019: 15
*  2/2019: 9
*  1/2019: 10

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

Total Matches: 44

Total Results (Limited by GitHUB API): 22

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [rvagg/go-car-example](https://github.com/rvagg/go-car-example)| 0 | 0 | 15| 2019-12-05 | 2019-12-05 |
| [ipld/go-ipld-prime-proto](https://github.com/ipld/go-ipld-prime-proto)| 0 | 0 | 44| 2019-10-25 | 2019-11-13 |
| [0zAND1z/ipld-crud](https://github.com/0zAND1z/ipld-crud)| 3 | 0 | 23| 2019-10-24 | 2019-11-21 |
| [filecoin-project/go-amt-ipld](https://github.com/filecoin-project/go-amt-ipld)| 1 | 1 | 24| 2019-08-28 | 2019-12-05 |
| [rvagg/go-ds-zipcar](https://github.com/rvagg/go-ds-zipcar)| 2 | 0 | 57| 2019-08-06 | 2019-08-13 |
| [Netflix/p2plab](https://github.com/Netflix/p2plab)| 23 | 7 | 16713| 2019-07-27 | 2019-11-07 |
| [ipld/go-ipld-schema](https://github.com/ipld/go-ipld-schema)| 4 | 0 | 84| 2019-07-01 | 2019-10-18 |
| [hsanjuan/ipfs-lite](https://github.com/hsanjuan/ipfs-lite)| 71 | 8 | 279| 2019-03-09 | 2019-11-04 |
| [whyrusleeping/sharray](https://github.com/whyrusleeping/sharray)| 2 | 0 | 6| 2019-01-16 | 2019-07-18 |
| [jonnycrunch/go-ipld-jsonld](https://github.com/jonnycrunch/go-ipld-jsonld)| 0 | 0 | 6| 2018-11-21 | 2018-07-13 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 130

Total Results (Limited by GitHUB API): 65

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [mikeal/csv-ipld-schema-gen](https://github.com/mikeal/csv-ipld-schema-gen)| 0 | 0 | 8| 2019-11-27 | 2019-12-03 |
| [simpleaswater/ipld](https://github.com/simpleaswater/ipld)| 0 | 0 | 18| 2019-10-05 | 2019-10-06 |
| [rvagg/js-ipld-hashmap](https://github.com/rvagg/js-ipld-hashmap)| 7 | 0 | 19| 2019-08-26 | 2019-08-28 |
| [ipld/metrics](https://github.com/ipld/metrics)| 0 | 0 | 1122| 2019-08-25 | 2019-12-05 |
| [vmx/ipld-stac](https://github.com/vmx/ipld-stac)| 1 | 0 | 13| 2019-08-22 | 2019-08-22 |
| [ipld/js-schema-gen](https://github.com/ipld/js-schema-gen)| 0 | 0 | 83| 2019-08-22 | 2019-12-03 |
| [rvagg/js-ds-zipcar](https://github.com/rvagg/js-ds-zipcar)| 8 | 0 | 30| 2019-08-12 | 2019-12-02 |
| [ipld/js-cli](https://github.com/ipld/js-cli)| 0 | 0 | 2| 2019-06-14 | 2019-08-14 |
| [ipld/js-printify](https://github.com/ipld/js-printify)| 5 | 1 | 7| 2019-06-04 | 2019-08-14 |
| [ipld/js-iq](https://github.com/ipld/js-iq)| 2 | 0 | 26| 2019-05-31 | 2019-08-14 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
