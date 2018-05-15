# Munin plugin for elasticsearch

A Munin plugin for monitoring Elasticsearch nodes. Written in Ruby, depends on [JSON gem](http://rubygems.org/gems/json). Compatible with Elasticsearch 5.x and 6.x.

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


## Installation

See the [Munin documentation](http://guide.munin-monitoring.org/) for complete instructions on [plugin usage](http://guide.munin-monitoring.org/en/latest/plugin/use.html). In short, once `elasticsearch_` is in your plugin directory, create symlinks for each desired mode in your Munin service dir (usually `/etc/munin/plugins/`). For example, to enable JVM monitoring:

```bash
ln -s /usr/local/munin/lib/plugins/elasticsearch_ /etc/munin/plugins/elasticsearch_jvm
```


## Configuration

You may also need to create a configuration file for the plugin, if the included defaults aren't suitable to your environment. Usually this would be `/etc/munin/plugin-conf.d/elasticsearch`.

### Variables
 * host - a elasticsearch node capable of providing stats interface (default localhost)
 * port - elasticsearch HTTP API port (default 9200)
 * node - the name of the node to monitor (default _local)

### Example Config
```
[elasticsearch_*]
env.host 10.1.2.14
env.port 9200
env.node pinky rat
```

## License

See the included [LICENSE](LICENSE.md) for rights and limitations under the terms of the MIT license.

