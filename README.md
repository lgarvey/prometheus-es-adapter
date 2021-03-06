# prometheus-es-adapter

## Overview

A read and write adapter for prometheus persistent storage

## Types

| Env Variables     | Default               | Description                                                        |
| ----------------- | --------------------- | ------------------------------------------------------------------ |
| ES_URL            | http://localhost:9200 | Elasticsearch URL                                                  |
| ES_USER           |                       | Elasticsearch User                                                 |
| ES_PASSWORD            |                       | Elasticsearch User Password                                        |
| ES_WORKERS        | 0                     | Number of batch workers                                            |
| ES_BATCH_COUNT    | 1000                  | Max items for bulk Elasticsearch insert operation                  |
| ES_BATCH_SIZE     | 4096                  | Max size in bytes for bulk Elasticsearch insert operation          |
| ES_BATCH_INTERVAL | 10                    | Max period in seconds between bulk Elasticsearch insert operations |
| ES_INDEX_MAXAGE   | 7d                    | Max age of Elasticsearch index before rollover                     |
| ES_INDEX_MAXDOCS  | 1000000               | Max documents in Elasticsearch index before rollover               |
| STATS             | true                  | Expose Prometheus metrics endpoint                                 |
| LISTEN            | :8080                 | TCP network address to start http listener on                      |
| VERSION           |                       | Display version and exit                                           |

## Getting started

## Contributing

Local development requires Go to be installed. On OS X with Homebrew you can just run `brew install go`.

Running it then should be as simple as:

```console
$ make build
$ ./bin/prometheus-es-adapter
```

### Testing

`make test`
