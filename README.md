# Munin plugin for elasticsearch

A simple Munin plugin for monitoring elasticsearch nodes in Ruby. Depends on [JSON gem](http://rubygems.org/gems/json).

## Supported Modes

### Cache
![](./screenshots/elasticsearch_cache-day.png)

`elasticsearch_cache` - field and query cache stats

### Docs
![](./screenshots/elasticsearch_docs-day.png)

`elasticsearch_docs` - document count

### Garbage Collection
![](./screenshots/elasticsearch_gc-day.png)

`elasticsearch_gc` - GC collections/sec

### Garbage Collection Running Time
![](./screenshots/elasticsearch_gc_time-day.png)

`elasticsearch_gc_time` - GC collection running time in ms

### JVM Heap
![](./screenshots/elasticsearch_jvm-day.png)

`elasticsearch_jvm` - JVM heap stats

### Operations
![](./screenshots/elasticsearch_ops-day.png)

`elasticsearch_ops` - index, get, search, delete operations/sec

### Store
![](./screenshots/elasticsearch_store-day.png)

`elasticsearch_store` - Size of index on disk

## Configuration

### Variables
 * host - a elasticsearch node capable of providing stats interface (default localhost)
 * port - elasticsearch HTTP API port (default 9200)
 * node - the name of the node to monitor (required)

### Example Config
```
[elasticsearch_*]
env.host 10.1.2.14
env.port 9200
env.node pinky rat
```

