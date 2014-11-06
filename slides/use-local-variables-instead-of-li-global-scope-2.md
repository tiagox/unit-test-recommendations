## Use local variables instead of `LI` global scope.

Maybe better.

```javascript
describe('Datatable', function () {
  'use strict';

  var datatable,
    advertisers = new LI.AdvertiserCollection(Bootstrapped.Advertisers);

  beforeEach(function() {
    datatable = new LI.AdvertisersDatatableView({
      collection: advertisers
    });
  });

});
```
