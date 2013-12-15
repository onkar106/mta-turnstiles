MTA Turnstile Data Parser
=========================

The MTA had a weekly snapshot of the entrances and exits for every transit turnstile in the city of New York.

It is in a bit of strange format and doesn't really lend itself well to visualizationg or further processing.

This project converts the data into an easily digestable format with location data added.

Installation
------------

    npm install -g mta-turnstiles

Install without the `-g` flag to use in custom scripts.

Usage
-----

### Command Line

    mta-turnstiles <url of weekly snapshot>

A list of snapshots can be found [here](http://www.mta.info/developers/turnstile.html).

You can also specify the `-f` flag with a filename to output directly to a file.

### Node

    var turnstiles = require('mta-turnstiles');

    turnstiles('http://www.mta.info/developers/data/nyct/turnstile/turnstile_131214.txt').pipe(process.stdout);

You can also use this module with a callback if you aren't into streams.

    turnstiles('http://www.mta.info/developers/data/nyct/turnstile/turnstile_131214.txt', function(data) {
        console.log(data);
    });

Issues
------

Report any issues via the issue tracker for this project.
