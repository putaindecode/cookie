![Cookie](https://raw.github.com/putaindecode/cookie/master/logo/logo.png)

Nom nom nom! The easy way to cook and eat cookies (yummy!) in ```#JavaScript```.

## Install via Bower

```shell
$ bower install putainde-cookie (--save-dev)
```

## Usage

### cookie

```javascript
// commonJS
var cookie = require("cookie")
// AMD
define(["cookie"], function(cookie){})
// otherwise
window.cookie
```

### Cookie.set

```javascript
cookie.set("my-own-cookie", "nom nom nom", {
  domain: ".wonderland.com",
  path: "/foo",
  expires: +new Date() + (Cookie.DAY * 4)
});

var expires = new Date();
expires.setTime(expires.getTime() + 8 * Cookie.DAY);
cookie.set("my-own-cookie", "nom nom nom", expires);
cookie.set("my-own-cookie", "nom nom nom");
```

### Cookie.get

```javascript
cookie.get("my-own-cookie"); // 'nom nom nom'
```

### Cookie.remove

```javascript
// bye-bye!
cookie.remove("my-own-cookie");
cookie.remove("my-own-cookie", {
  domain: ".wonderland.com",
  path: "/foo"
});
```

## Sugar!

Cookie fits well with the excellent lib [moment.js](http://momentjs.com/).

First of all, install moment:

```shell
$ bower install moment
```

Now, you can use something like this:

```javascript
// Cookie should be eaten before the end of the day
cookie.set("gingerbread", "excellent", {
  expires: moment().endOf('day')
});
```

## Attribution

<a href="http://thenounproject.com/noun/cookie/#icon-No17125" target="_blank">Cookie</a> designed by <a href="http://thenounproject.com/car.lancaster" target="_blank">Caroline Lancaster</a> from The Noun Project.
