##  Test behavior instead of implementation

This could be a better approach

```javascript
describe('Some view', function () {
  'use strict';

  var fixture = readFixtures('fixture.txt'),
    someView = new SomeView();

  it('should hide some element if some method its called', function () {
    $('body').html(fixture);

    someView.someMethodThatHideSomething();

    expect($('.someElement')).not.toBeHidden();
  });

});
```
