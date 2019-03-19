# NodeJS - Working with files, Modularity of Node

## Learning Competencies
By the end of this day you should be able to
- Handle File system in Node.js
- Manipulate files using File system module
  - Read, Create, Update, Delete & Rename
- Understand how to create your own module
- Publishing your module through npm, github etc.

## Overview

### Node.js File system module

The Node.js file system module allow you to work with the file system on your computer. We all know to include the File System module, use the require() method:

```js
var fs = require('fs');
```

Common use for the File System module:

- Read files
- Create files
- Update files
- Delete files
- Rename files

#### Read Files

The `fs.readFile()` method is used to read files on your computer.

```js
var http = require('http');
var fs = require('fs');
http.createServer(function (req, res) {
  fs.readFile('demofile1.html', function(err, data) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write(data);
    res.end();
  });
}).listen(8080);
```

#### Create Files

The File System module has methods for creating new files:

- `fs.appendFile()`
- `fs.open()`
- `fs.writeFile()`

The `fs.appendFile()` method appends specified content to a file. If the file does not exist, the file will be created:

```js
var fs = require('fs');

fs.appendFile('mynewfile1.txt', 'Hello content!', function (err) {
  if (err) throw err;
  console.log('Saved!');
});
```

The `fs.open()` method takes a "flag" as the second argument, if the flag is "w" for "writing", the specified file is opened for writing. If the file does not exist, an empty file is created:

```js
var fs = require('fs');

fs.open('mynewfile2.txt', 'w', function (err, file) {
  if (err) throw err;
  console.log('Saved!');
});
```

The `fs.writeFile()` method replaces the specified file and content if it exists. If the file does not exist, a new file, containing the specified content, will be created:

```js
var fs = require('fs');

fs.writeFile('mynewfile3.txt', 'Hello content!', function (err) {
  if (err) throw err;
  console.log('Saved!');
});
```

#### Update Files

The File System module has methods for updating files:

- `fs.appendFile()`
- `fs.writeFile()`

The `fs.appendFile()` method appends the specified content at the end of the specified file:

```js
var fs = require('fs');

fs.appendFile('mynewfile1.txt', ' This is my text.', function (err) {
  if (err) throw err;
  console.log('Updated!');
});
```

The `fs.writeFile()` method replaces the specified file and content:

```js
var fs = require('fs');

fs.writeFile('mynewfile3.txt', 'This is my text', function (err) {
  if (err) throw err;
  console.log('Replaced!');
});
```

#### Delete Files

To delete a file with the File System module,  use the fs.unlink() method.

The `fs.unlink()` method deletes the specified file:

```js
var fs = require('fs');

fs.unlink('mynewfile2.txt', function (err) {
  if (err) throw err;
  console.log('File deleted!');
});
```

#### Rename Files

To rename a file with the File System module,  use the `fs.rename()` method.

```js
var fs = require('fs');

fs.rename('mynewfile1.txt', 'myrenamedfile.txt', function (err) {
  if (err) throw err;
  console.log('File Renamed!');
});
```


## Modularity of Node

Now you all know what is module is, look into how to create your own module

- Complete core blocks

# Exploration

 - [File system](https://www.npmjs.com/package/file-system)
 - [More about File system module](https://www.tutorialspoint.com/nodejs/nodejs_file_system)
 - [Node.js file system official Doc.](https://nodejs.org/api/fs.html)
 - [Node Modules](https://www.npmjs.com/package/node-modules)
 - [Creating node modules](https://codeburst.io/how-to-create-and-pblish-your-first-node-js-module-444e7585b738)
 - [`npm install`](https://docs.npmjs.com/cli/install)
 - [Javscript import and require](https://medium.com/@thejasonfile/a-simple-intro-to-javascript-imports-and-exports-389dd53c3fac#ed30)
 - [Require and Exports](https://medium.freecodecamp.org/requiring-modules-in-node-js-everything-you-need-to-know-e7fbd119be8)
