*This repository is a mirror of the [component](http://component.io) module [nathan7/snakeize](http://github.com/nathan7/snakeize). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/nathan7-snakeize`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# snakeize 

recursively transform key strings from camel-case to underscore-style.
Derives directly from [substack](https://github.com/substack)'s [camelize](https://github.com/substack/camelize)

[![build status](https://secure.travis-ci.org/nathan7/snakeize.png)](http://travis-ci.org/nathan7/snakeize)

[![browser support](https://ci.testling.com/nathan7/snakeize.png)](http://ci.testling.com/nathan7/snakeize)

# example

``` js
var snakeize = require('snakeize');
var obj = {
    feeFieFoe: 'fum',
    beepBoop: [
        { 'abcXyz': 'mno' },
        { 'FooBar': 'baz' },
        { 'CheeseID': 'wensleydale' }
    ]
};
var res = snakeize(obj);
console.log(JSON.stringify(res, null, 2));
```

output:

```
{
  "fee_fie_foe": "fum",
  "beep_boop": [
    {
      "abc_xyz": "mno"
    },
    {
      "foo_bar": "baz"
    },
    {
      "cheese_id": "wensleydale"
    }
  ]
}
```

# methods

``` js
var snakeize = require('snakeize')
```

## snakeize(obj)

Convert the key strings in `obj` from camel-case to underscore-stlye recursively.

# install

With [npm](https://npmjs.org) do:

```
npm install snakeize
```

To use in the browser, use [browserify](http://browserify.org) or [component](http://github.com/component):
```
component install nathan7/snakeize
```

# license

MIT
