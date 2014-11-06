## Specs should be code examples

```javascript
describe('LI.DatatableView', function() {
  'use strict';

  var genericDatatableFixture = readFixtures('GenericDatatableFixture.txt');

  it('should render', function () {
    // Arrange / Given
    $('body').html(genericDatatableFixture);

    var timestamp = Date.now(),
      collection = new LI.Collection(bootstrappedData),
      datatable = new LI.DatatableView({
        el: '#GenericDatatableContainer',
        collection: collection,
        timestamp: timestamp
      });

    // Act / When
    datatable.render({
      name: 'generics',
      container: datatable.$el.selector,
      template: $('#generic-table-template').html(),
      data: datatable.collection.toJSON()
    });

    jasmine.waitsForDatatableViewRender(timestamp, datatable);

    runs(function() {
      // Assert / Then
      expect(datatable.$el).toContain('.liDataTable');

      // Annihilate
      $('body').html('');
    });
  });

});
```
