## Downloads

- [Tools for Users](#users)
- [Packages for Developers](#dev)
- [Editor Support](#ed)
- [Tools with native support](#native)

## <a id="users"></a> Tools for Users

You can always check the syntax of an Hjson file by simply running `hjson FILE`. It will show you the exact location if it contains any errors.

If an application does not yet use native Hjson configs you use it to convert your config to JSON.

The preferred tool works on all operating systems and only requires node.js.

### Setup

- Install [**node.js**](http://nodejs.org/) if it's not already on your system
- Install the Hjson tool by running `npm install hjson -g` on the command line

### Usage

- `hjson FILE`

  Loads a `.json` or `.hjson` file and outputs it as Hjson.

  You can also use it to checks the specified file for syntax errors (it will print the exact location).

  E.g. `hjson config.json`

- `hjson -j FILE`

  Will convert an Hjson file to JSON.

  E.g. `hjson -j config.hjson > config.json`.

### Alternative tools

If you don't want to install node.js you can also use one of the following tools.

#### Python

- Install [**Python**](https://www.python.org/)
- Install [Hjson](https://pypi.python.org/pypi/hjson) with `pip install hjson`
- `python -m hjson.tool file.json` will convert to Hjson.
- `python -m hjson.tool -j file.hjson` will convert to JSON.

#### chocolatey (Windows only)

- Install [chocolatey](https://chocolatey.org)
- Install [Hjson](https://chocolatey.org/packages/hjson) with `choco install hjson`
- `hjsonc file.json` will convert to Hjson.
- `hjsonc -j file.hjson` will convert to JSON.

## <a id="dev"></a> Packages for Developers

Platform | Source | Package
-------- | ------ | -------
JavaScript, Node.js & Browser | [hjson-js](https://github.com/laktak/hjson-js) | [![NPM version](https://img.shields.io/npm/v/hjson.svg?style=flat-square)](http://www.npmjs.com/package/hjson)
Java     | [hjson-java](https://github.com/laktak/hjson-java) | [![Maven Central](https://img.shields.io/maven-central/v/org.hjson/hjson.svg?style=flat-square)](http://search.maven.org/#search&#124;ga&#124;1&#124;g%3A%22org.hjson%22%20a%3A%22hjson%22)
Python   | [hjson-py](https://github.com/laktak/hjson-py) | [![PyPI version](https://img.shields.io/pypi/v/hjson.svg?style=flat-square)](https://pypi.python.org/pypi/hjson)
C#, .Net | [hjson-cs](https://github.com/laktak/hjson-cs) | [![nuget version](https://img.shields.io/nuget/v/Hjson.svg?style=flat-square)](https://www.nuget.org/packages/Hjson/)
PHP      | [hjson-php](https://github.com/laktak/hjson-php) | [![Packagist](https://img.shields.io/packagist/v/laktak/hjson.svg?style=flat-square)](https://packagist.org/packages/laktak/hjson)

#### Partial implementations

Platform | Description | Source |
-------- | ------ | -------
Go       | Parser and unmarshaller using a [slightly different syntax](https://github.com/client9/xson/tree/master/hjson#differences-andor-bugs) | [xson](https://github.com/client9/xson)
C        | jzon variant, based on Hjson | [jzon-c](https://github.com/KarlZylinski/jzon-c)

Please [open an issue](https://github.com/laktak/hjson/issues) if you port Hjson to another platform/language.

## <a id="ed"></a> Editor Support

Name     | Source | Package
-------- | ------ | -------
Atom | [language-hjson](https://github.com/dannyfritz/language-hjson) | [package](https://atom.io/packages/language-hjson)
Sublime Text / TextMate | [sublime-hjson](https://github.com/laktak/sublime-hjson) | [packagecontrol.io](https://packagecontrol.io/packages/Hjson)
Notepad++    | [npp-hjson](https://github.com/laktak/npp-hjson) | see source

## <a id="native"></a> Tools with native support

Name     | Link | Details
-------- | ---- | -------
**any-json**: convert (almost) anything to JSON | [![NPM version](https://img.shields.io/npm/v/any-json.svg?style=flat-square)](http://www.npmjs.com/package/any-json) | [see readme](https://github.com/laktak/any-json#usage)
**gulp**: the streaming build system | [![NPM version](https://img.shields.io/npm/v/gulp-hjson.svg?style=flat-square)](http://www.npmjs.com/package/gulp-hjson) | [see readme](https://github.com/laktak/gulp-hjson#usage)
**grunt**: the JavaScript task runner | [![NPM version](https://img.shields.io/npm/v/grunt-hjson.svg?style=flat-square)](http://www.npmjs.com/package/grunt-hjson) | [see readme](https://github.com/laktak/grunt-hjson#usage)
**hjsonify**: a browserify transform to require Hjson files | [![NPM version](https://img.shields.io/npm/v/hjsonify.svg?style=flat-square)](http://www.npmjs.com/package/hjsonify) | [see readme](https://github.com/dannyfritz/hjsonify#usage)
**node-config**: node.js application configuration | [![NPM version](https://img.shields.io/npm/v/config.svg?style=flat-square)](http://www.npmjs.com/package/config) | [see wiki](https://github.com/lorenwest/node-config/wiki/Configuration-Files#human-json---hjson)
**nconf**: hierarchical node.js configuration | [![NPM version](https://img.shields.io/npm/v/nconf.svg?style=flat-square)](http://www.npmjs.com/package/nconf) | `nconf.file({ file: 'file.hjson',`<br>`   format: require('hjson').rt });`<br>`// round trips your comments`
**rc**: non-configurable configuration loader for lazy people. | [![NPM version](https://img.shields.io/npm/v/rc.svg?style=flat-square)](http://www.npmjs.com/package/rc) | `var conf=require('rc')('appname', {/*defaults*/},`<br>`  null, require('hjson').parse);`
