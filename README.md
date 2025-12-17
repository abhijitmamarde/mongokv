[![Logo](https://patx.github.io/mongokv/logo.png)](https://patx.github.io/mongokv)
is a tiny sync/async key-value store backed by PyMongo that provides a 
dead simple Redis-like API (`set`, `get`, etc). It is safe across threads, processes, 
and ASGI workers. For help getting started, installation, advanced examples and more 
read the [API Docs and User Guide here](https://patx.github.io/mongokv).


```python
>>> from mongokv import Mkv

>>> db = Mkv('mongodb://localhost:27071')
>>> db.set('hello', {'name': 'world', 'status': 'green'})

>>> db.get('hello')
{'name': 'world', 'status': 'green'}
```
