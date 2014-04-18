# node-box-sdk [![Build Status](https://travis-ci.org/adityamukho/node-box-sdk.svg?branch=master)](https://travis-ci.org/adityamukho/node-box-sdk) [![NPM version](https://badge.fury.io/js/node-box-sdk.png)](http://badge.fury.io/js/node-box-sdk) [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)

[![Npm Downloads](https://nodei.co/npm/node-box-sdk.png?downloads=true&stars=true)](https://nodei.co/npm/node-box-sdk.png?downloads=true&stars=true)

Node.js client for the Box.com Content API.

**THIS MODULE IS UNDER CONSTRUCTION.**

## Getting Started
Install the module with: `npm install box-sdk`

```javascript
var box_sdk = require('box-sdk')({
	'log-level': 'debug'
});
//OR
//var box_sdk = require('box-sdk')(); //Default log-level: info

//Default host: localhost
var box = box_sdk.Box('client_id', 'client_secret', port /*, host, customLogger */);
var connection = box.getConnection('some.email@example.com');

//Navigate user to the auth URL
console.log(connection.getAuthURL());

connection.on('tokens.set', function (data, envelope) {
	connection.listFolders(0, function (err, result) {
		if (err) {
			console.error(err);
		}
		console.dir(result);
	});
});
```

## Documentation
_(Coming soon)_

## Examples
_(Coming soon)_

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_

## License
Copyright (c) 2014 Aditya Mukhopadhyay
Licensed under the MIT license.
