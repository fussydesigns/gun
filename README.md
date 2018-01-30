# Marksman

Replacement function for `gun`'s internal `.path()` function, except replacing the core delimiter from a period to a forward-slash.

## Using in applications

```
npm i --save marksman gun
```

```
var Gun = require('gun');
Gun.chain.path = require('marksman');
var gun = new Gun();

var x = { object: true };
// the following lines are equivalent:

gun.get('first').get('second').get('third').put(x);

gun.path(['first', 'second', 'third']).put(x);

gun.path('first/second/third').put(x);
```

## License

This is a fork of [gun.js](//github.com/amark/gun) with everything else stripped

Designed with ♥ by Mark Nadal, the GUN team, and many amazing contributors.

Openly licensed under [Zlib / MIT / Apache 2.0](https://github.com/amark/gun/blob/master/LICENSE.md).
