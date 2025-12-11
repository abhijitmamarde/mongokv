mkvDB is a unified sync + async key-value store backed by MongoDB. It gives you a 
dead-simple Redis-like API (set, get, remove, etc.) while letting MongoDB handle all 
the heavy concurrency lifting — meaning it’s safe across threads, processes, and 
ASGI workers out of the box. Sync usage uses `MongoClient` (thread-safe). Async usage
uses `AsyncMongoClient` (non-blocking, ASGI/uvicorn safe). Same API either way.
[Read the docs here.](https://thoughts.harrisonerd.com/post/693a32cee5c413ce5f061c19)

```
from mkvdb import Mkv

db = Mkv("mongodb://localhost:27017")

# Sync
db.set("key", "value")
db.get("key")

# Async
await db.set("a", 123)
val = await db.get("a")
```

