##  What to spy (mocking)

```javascript
it('should call to "LI.Validation.update()" if the "LI.Validation" is in use and a row is clicked', function () {
  jasmine.waitsForDatatableViewRender(timestamp, datatable);

  runs(function() {
    var spyValidationInUse = spyOn(LI.Validation, 'inUse').andCallFake(function () {
        return true;
      }),
      spyValidationUpdate = spyOn(LI.Validation, 'update');

    $(datatable.$el.find('tbody tr')[2]).trigger('click');

    expect(spyValidationInUse).toHaveBeenCalled();
    expect(spyValidationUpdate).toHaveBeenCalled();

    spyValidationInUse.reset();
    spyValidationUpdate.reset();
  });
});
```
