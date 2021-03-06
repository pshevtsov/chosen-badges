chosen-badges
=============

Show custom badges on chosen items

Dependencies
------------
Chosen jQuery plugin

Usage
-----
```javascript
$('#some .selector').chosenBadges( options ).chosen();
```

Options
-------
### `value`
Default value. May be either a function or a value:
```javascript
var options = {
  value: function(v) { return someMethod(v); }
};
```
```javascript
var options = {
  value: 42
};
```

### `numbering`
Use numbering widget. May be boolean (`true` or `false` (default)) or object with `min`, `max` and `step` properties:
```javascript
var options = {
  numbering: {
    min: 0,
    max: 100,
    step: 10
  }
};
```
`min`, `max` and `step` properties may be functions as well:
```javascript
var options = {
  numbering: {
    min: function (key, plugin) {
      …
    }
  }
};
```

Events
------

### `chosenBadges:click`
The event is fired when user clicks on a badge.

Additional event properties:
* `badge`: plugin instance,
* `key`: badge key,
* `value`: badge value.

Methods
-------
### `get(key)`
Get badge value by key.

### `get()`
Get all badges.

### `getValue(key)`
Compute badge value for key using `options.value` property.

### `set(key, value)`
Set badge value for key.

### `set(obj)`
Set all badges.

Demo
----
[Demo](http://pshevtsov.github.io/chosen-badges/demo.html)

License
-------
MIT
