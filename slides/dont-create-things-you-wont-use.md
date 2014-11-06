## Don't create **things** you won't use

```javascript
describe('Datatable', function () {
  'use strict';

  beforeEach(function() {
    LI.DataTable = new LI.DatatableView({
      collection: LI.Advertisers
    });

    // spies
    spyOn(datatable, 'updateDataBinding').andCallThrough();
    spyOn(datatable, 'render').andCallThrough();
    spyOn($.fn, 'showLoader');
    spyOn($.fn, 'hide');
    spyOn($.fn, 'remove');
    spyOn($.fn, 'find');
  });

});
```
