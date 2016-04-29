Sprockets Example
=================

```
bin/rails s
curl http://localhost:3000/assets/example.js
```

Shows problem with adding newlines to Javascript files in development
as described in https://github.com/rails/sprockets/issues/291.

example.js should look like:

```
/******/ function testRails() {
/******/ }
```

But curl returns:

```
/******/
 function testRails() {
/******/ }
```

Note the newline inserted after the first comment.
