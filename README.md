# Embulk output plugin for Redis

## Generic

### Overview

* **Plugin type**: output
* **Resume supported**: no

## Configuration

- **host**: Hostname of the Redis server (string, default: "localhost")
- **port**: Port of the Redis server (integer, default: 6379)
- **db**: Database number (integer, default: 0)
- **key_prefix**: Key prefix for input/output plugin (string, default:"")
- **encode**: Encoding in Redis (string, default: "json")
 - json: Stored as a JSON string. GET/SET commands can access it
 - hash: Stored as a Hash. H* commands such as HMGET/HMSET can access it
- **key**: Column name used for a key in Redis (string, required)

### Example

```yaml
out:
  type: redis
  host: localhost
  port: 6379
  db: 0
  key: id
  key_prefix: user_
  encode: json
```

