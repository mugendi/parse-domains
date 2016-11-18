parse-domains
========================================================================
**Splits an url into sub-domain, domain and top-level-domain.**

Setup
------------------------------------------------------------------------

[![npm status](https://nodei.co/npm/parse-domains.png?downloads=true&stars=true)](https://npmjs.org/package/parse-domains)

This module was a hack of [parse-domain](https://www.npmjs.com/package/parse-domain) hence the name similarity. But I soon discovered that the premise of using a list of known tlds was a faulty one as new top level domains are introduced every so often.

Rewrote it using the awesome [url](https://www.npmjs.com/package/url) module.

```javascript
var parse = require('./lib/parseDomain');

var url = 'https://github.com/mugendi/parse-domains';

console.log( parse(url) )
```


API
------------------------------------------------------------------------

### parseDomain(url: String): ParsedDomain|null

Returns `null` if `url` has an unknown tld or if it's not a valid url.

### ParsedDomain

```
{
    tld: String,
    domain: String,
    subdomain: String,
    dtld: String
}
```
