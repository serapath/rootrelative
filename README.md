# rootrelative
enable require(rootRelativePath) by using an absolute path starting from the projects root directory
`npm install rootrelative`

consider the following project structure:
* myProject/
  * index.js
  * lib/
    * index.js
    * abc.js
    * def.js
    * helper/
      * xyz.js

__[xyz.js]__
```
var my = require('rootrelative');
var
  myProject = require(my('')),
  abc       = require(my('lib/abc.js'),
  lib       = require(my('lib')
;

```
