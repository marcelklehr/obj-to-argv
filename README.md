# obj-to-argv
There are plenty of packages out there that allow you to parse command line arguments, stuff like `foo --three=3 --jump=yay`.

This library provides the inverse functionality. Pass it an object and it spits out the corresponding command line params.

## Usage
```js
var toArgv = require('obj-to-argv')

var args = toArgv({
  afloat: .5
, tuut: 'sob'
, foo: {bar: 5, so: 6}
})

console.log(args) // ["--afloat=0.5", "--tuut=sob", "--foo.bar=5", "--foo.so=6"]
```

## API

### toArgv(obj, [args, [prefix]])
 * obj {Object} The object to stringify
 * args {args} An existing array of args where these should be appended
 * prefix {String} Will be used instead of '--'

## License
MIT