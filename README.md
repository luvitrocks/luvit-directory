# Directory

> Middleware for [luvit.io](http://luvit.io) and [Utopia](https://github.com/luvitrocks/utopia) that serves pages that contain directory listings for a given path.

## Install

```bash
lit install voronianski/directory
```

## API

### ``directory(root, options)``

Serve directory listings with the given `root` path

### Options

- ``hidden`` - display hidden dot files, defaults to ``false``
- ``filter`` - apply custom filter function to files, defaults to ``false``

## Example

```lua
local path = require('path')
local Utopia = require('utopia')
local directory = require('directory')

local __dirname = module.dir
local app = Utopia:new()

local publicDir = path.join(__dirname, 'public')

app:use(directory(publicDir))

app:listen(8080)
```

## License

MIT Licensed

Copyright (c) 2014-2016 Dmitri Voronianski [dmitri.voronianski@gmail.com](mailto:dmitri.voronianski@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
