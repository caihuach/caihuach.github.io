## js does not support bigint well

when I use `JSON.parse()` for some json string, it gives back some wrong field for bigint

## solution

use [json-bigint](https://github.com/sidorares/json-bigint) to handle this

sometimes you may want to use the following, before SQL insert to bigint field

```js
var JSONbigString = require('json-bigint')({"storeAsString": true});
var withString = JSONbigString.parse(key);
```
