Version 0.2.6
-------------
- Fixed references to cycle.js and underscore-min.js
- Using underscore templates to serve up the client.js file with the correct configured port for socket.io to connect to

Version 0.2.5
-------------
- Fixed bug where results of commands weren't being decycled before being sent to the client
- Allow second argument to nomo.cmd(...) on client to be optional - if no args are used or required, just pass the callback as the second argument instead

Version 0.2.4
-------------
- Fixed a bug with cycle.js causing it to filter out functions any potentially other data types
- Now sends full object representation including functions, which are normally stripped out by converting to JSON

Version 0.2.3
-------------
- Added missing 'profiler.getData' and 'profiler.clearData' commands to client side
- Changed the way commands work for added security and to make the command interface available the application developer for any desired use
- Added support for logging cyclical objects using cycle.js from https://github.com/douglascrockford/JSON-js (Thanks Douglas Crockford)
- Cleaned up code a bit including moving all code related files (except index.js) to `src/` directory and breaking client HTML file into
  a separate Underscore template file
- Renamed global object from 'nm' to 'nomo'
- Added 'revertConsole()' method
- Removed `active` config option for profiler and any documentation referencing configuring the profiler until there is something to configure
- Standardized a method of documentation and documented everything well

Version 0.2.0
-------------
- Added profiling functionality
- Added ability to send commands to the Node.js server from the web browser

Version 0.1.2
-------------
- Fixed a bug causing NodeMonkey to crash the app it's included in

Version 0.1.1
-------------
- Changed default port to 50500
- Fixed logging issue causing messages to only be sent to the client on initial connection
- Fixed websocket reconnection problem
- Added buffering on Firefox if Firebug isn't open on initial page load so messages can be displayed once it is
- Dumps instructions to the console when started. Added `silent` option to disable this behavior.
