## Remove unnecessary tests

```javascript
describe('Some view', function () {
  'use strict';

  // This's fine just to keep a placeholder for a while
  it('should have some method', function () {
    expect(SomeView.someMethod).toBeDefined();
  });

});
```
