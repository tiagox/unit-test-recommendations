## Use local variables instead of `LI` global scope.

This could conflict with the real LI global scope.

```javascript
describe('Datatable', function () {
  'use strict';

  LI.Advertisers = new LI.AdvertiserCollection(Bootstrapped.Advertisers);

  beforeEach(function() {
    LI.DataTable = new LI.DatatableView({
      collection:
    });
  });

});
```
