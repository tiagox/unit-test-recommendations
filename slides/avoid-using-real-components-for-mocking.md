## Avoid using real components for mocking.

This was part of the spec file for `DatatableView.js`.

```javascript
it('can be initialized by subclass', function() {
  $('body').html(fixture);

  LI.Advertisers = new LI.AdvertiserCollection(Bootstrapped.Advertisers);

  var advertisersDataTable = new LI.AdvertisersDatatableView({
    collection: LI.Advertisers
  });

  expect(advertisersDataTable.$el).toContain('.liDataTable');

  $('body').html('');
});
```

Also, test  the component directly.
