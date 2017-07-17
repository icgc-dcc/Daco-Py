# DacoClient

Bare bones wrapper class for communicating to ICGC's DACO API through OAuth

## Usage

```python
from daco_client import DacoClient


daco = DacoClient(base_url='https://my.daco.site.org/',
                  client_key='myclientkey',
                  client_secret='myclientsecret',
                  token='myaccesstoken',
                  token_secret='myaccesstokensecret')

daco.get_daco_status('foo.bar@gmail.com')
```

This should return something like:

```
{'user': {'openid': 'foo.bar@gmail.com', 'csa': False, 'userinfo': [{'uid': '1', 'name': 'foobar', 'email': 'foo.bar@my.org'}]}}
```