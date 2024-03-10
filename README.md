# list of Redis commands commonly used in Python applications, formatted for use with the redis-py module:

```python
# String Commands
redis.set(key, value)
redis.get(key)
redis.delete(*keys)
redis.incr(key, amount=1)
redis.decr(key, amount=1)
redis.exists(key)
redis.expire(key, seconds)
redis.ttl(key)
redis.keys(pattern)
redis.type(key)
redis.rename(old_key, new_key)
redis.renamenx(old_key, new_key)
redis.move(key, db)
redis.mset(mapping)
redis.mget(keys)

# Hash Commands
redis.hset(name, key, value)
redis.hget(name, key)
redis.hgetall(name)
redis.hdel(name, *keys)
redis.hexists(name, key)
redis.hkeys(name)
redis.hlen(name)
redis.hmget(name, keys)
redis.hmset(name, mapping)
redis.hvals(name)
redis.hincrby(name, key, amount=1)
redis.hincrbyfloat(name, key, amount=1.0)

# List Commands
redis.rpush(key, *values)
redis.lpush(key, *values)
redis.llen(key)
redis.lrange(key, start, end)
redis.lindex(key, index)
redis.lset(key, index, value)
redis.lrem(key, value, num=0)
redis.lpop(key)
redis.rpop(key)
redis.rpoplpush(source, destination)

# Set Commands
redis.sadd(key, *values)
redis.srem(key, *values)
redis.spop(key)
redis.srandmember(key, number=None)
redis.sismember(key, value)
redis.scard(key)
redis.smembers(key)
redis.sunion(keys, *args)
redis.sinter(keys, *args)
redis.sdiff(keys, *args)

# Sorted Set Commands
redis.zadd(name, mapping)
redis.zrem(name, *values)
redis.zrange(name, start, end, withscores=False)
redis.zrevrange(name, start, end, withscores=False)
redis.zrangebyscore(name, min, max, withscores=False)
redis.zcard(name)
redis.zscore(name, value)
redis.zincrby(name, value, amount=1)
redis.zcount(name, min, max)
redis.zremrangebyrank(name, start, end)
redis.zremrangebyscore(name, min, max)
redis.zremrangebylex(name, min, max)

# List Blocking Commands
redis.blpop(keys, timeout)
redis.brpop(keys, timeout)
redis.brpoplpush(source, destination, timeout)

# Pub/Sub Commands
redis.publish(channel, message)
redis.subscribe(*channels)
redis.unsubscribe(*channels)
redis.psubscribe(*patterns)
redis.punsubscribe(*patterns)

# Transaction Commands
redis.watch(*keys)
redis.unwatch()
redis.multi()
redis.execute()
redis.discard()

# Connection Commands
redis.auth(password)
redis.select(db)
redis.echo(message)
redis.quit()

# Server Commands
redis.info(section=None)
redis.monitor()
redis.bgsave()
redis.bgrewriteaof()
```
