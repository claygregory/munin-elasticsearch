#Munin plugin for elasticsearch

A simple Munin plugin for monitoring elasticsearch nodes in Ruby. Depends on [JSON gem](http://rubygems.org/gems/json).

##Supported Modes

 * cache - field and filter cache stats
 * docs - document count
 * gc - GC collections/sec
 * jvm - JVM heap stats
 * ops - index, get, search, delete operations/sec
 * store - size of index

##Configuration

###Variables
 * host - a elasticsearch node capable of providing stats interface (default localhost)
 * port - elasticsearch HTTP API port (default 9200)
 * node - the name of the node to monitor (required)

###Example Config
```
[elasticsearch_*]
env.host 10.1.2.14
env.port 9200
env.node pinky rat
```

