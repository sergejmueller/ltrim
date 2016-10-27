ltrim
============

`ltrim` Node.js module returns a string with whitespace (or other characters) stripped from the beginning of a string. Without dependencies and library bloat.


[![Dependency Status](https://david-dm.org/sergejmueller/ltrim.svg)](https://david-dm.org/sergejmueller/ltrim)
[![Code Climate](https://codeclimate.com/github/sergejmueller/ltrim/badges/gpa.svg)](https://codeclimate.com/github/sergejmueller/ltrim)
[![Build Status](https://travis-ci.org/sergejmueller/ltrim.svg?branch=master)](https://travis-ci.org/sergejmueller/ltrim)
[![Known Vulnerabilities](https://snyk.io/test/github/sergejmueller/ltrim/badge.svg)](https://snyk.io/test/github/sergejmueller/ltrim)


Install
-----

```bash
npm install ltrim
```

*or*

```bash
yarn add ltrim
```


Usage
-----

```javascript
ltrim ( str [, chars ] )
```

Parameter | Description
--- | ---
`str` | The input string
`chars` | Characters that you want to be stripped

Without the second parameter, `ltrim` will strip whitespaces (spaces, tabs and new lines).


Examples
-----

```javascript
var ltrim = require( 'ltrim' );

/* Strip whitespace from the beginning of a string */
ltrim( '    Hello    ' ) + ' World' // →Hello     World

/* Strip multiple special chars from the beginning of a string */
ltrim( '... Hello World ...', ' .' ); // →Hello World ...

/* Strip multiple chars from the beginning of a string */
ltrim( 'Hello World', 'Hdle' ); // →o World

/* Strip url protocol from the beginning of a string */
ltrim( 'https://goo.gl/', '/:htps' ); // →goo.gl/
```
