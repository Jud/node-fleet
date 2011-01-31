node-fleet
==========

The ´´node-fleet´´ module provides a FleetDB (http://fleetdb.org/) client for Node.js(http://nodejs.org/).

Here is a quick example how to use the module:

	var sys = require('sys'),
	    fleetdb = require('./inc-js/fleetdb');

	var db = new fleetdb.fleetDB();
	    db.open('localhost');

	db.query(['ping'], function(status, data) {
  		sys.puts('Status: ' + status + ' Data:' + data);
	});

	db.close();
