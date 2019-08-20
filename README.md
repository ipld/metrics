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
*  8/2019: 13
*  7/2019: 16
*  6/2019: 13
*  5/2019: 22
*  4/2019: 24
*  3/2019: 13
*  2/2019: 13
*  1/2019: 12
*  12/2018: 8
*  11/2018: 12
*  10/2018: 14
*  9/2018: 10

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

Total Matches: 36

Total Results (Limited by GitHUB API): 18

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [rvagg/go-ds-zipcar](https://github.com/rvagg/go-ds-zipcar)| 0 | 0 | 57| 2019-08-06 | 2019-08-13 |
| [Netflix/p2plab](https://github.com/Netflix/p2plab)| 5 | 3 | 7103| 2019-07-27 | 2019-08-20 |
| [whyrusleeping/ipld-schema](https://github.com/whyrusleeping/ipld-schema)| 4 | 0 | 15| 2019-07-01 | 2019-07-08 |
| [hsanjuan/ipfs-lite](https://github.com/hsanjuan/ipfs-lite)| 42 | 3 | 246| 2019-03-09 | 2019-08-12 |
| [whyrusleeping/sharray](https://github.com/whyrusleeping/sharray)| 2 | 0 | 6| 2019-01-16 | 2019-07-18 |
| [jonnycrunch/go-ipld-jsonld](https://github.com/jonnycrunch/go-ipld-jsonld)| 0 | 0 | 6| 2018-11-21 | 2018-07-13 |
| [ipld/go-ipld-prime](https://github.com/ipld/go-ipld-prime)| 19 | 5 | 427| 2018-10-31 | 2019-08-15 |
| [qri-io/go-ipld-manifest](https://github.com/qri-io/go-ipld-manifest)| 6 | 2 | 5| 2018-09-25 | 2018-09-25 |
| [ipfs/go-unixfs](https://github.com/ipfs/go-unixfs)| 43 | 16 | 26665| 2018-07-30 | 2019-07-26 |
| [computes/go-ipld-polymorph](https://github.com/computes/go-ipld-polymorph)| 1 | 4 | 46| 2018-02-05 | 2018-11-12 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 118

Total Results (Limited by GitHUB API): 59

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [rvagg/js-ds-zipcar](https://github.com/rvagg/js-ds-zipcar)| 2 | 0 | 25| 2019-08-12 | 2019-08-13 |
| [ipld/js-cli](https://github.com/ipld/js-cli)| 0 | 0 | 2| 2019-06-14 | 2019-08-14 |
| [ipld/js-printify](https://github.com/ipld/js-printify)| 5 | 1 | 7| 2019-06-04 | 2019-08-14 |
| [ipld/js-iq](https://github.com/ipld/js-iq)| 2 | 0 | 26| 2019-05-31 | 2019-08-14 |
| [ipld/js-composites](https://github.com/ipld/js-composites)| 5 | 2 | 52| 2019-05-27 | 2019-08-08 |
| [ipld/js-block](https://github.com/ipld/js-block)| 0 | 1 | 10| 2019-05-19 | 2019-06-10 |
| [ipld/js-get-codec](https://github.com/ipld/js-get-codec)| 0 | 1 | 12| 2019-05-09 | 2019-08-14 |
| [ipld/js-path-level-one](https://github.com/ipld/js-path-level-one)| 0 | 0 | 7| 2019-05-07 | 2019-08-14 |
| [ipld/js-codec-interface](https://github.com/ipld/js-codec-interface)| 2 | 0 | 13| 2019-05-03 | 2019-08-14 |
| [mikeal/js-ipld-http-storage](https://github.com/mikeal/js-ipld-http-storage)| 1 | 0 | 15| 2019-05-02 | 2019-08-19 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
