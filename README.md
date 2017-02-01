# iml4hci-assignment2

## To run the UDP->TCP bridge:
1. Install node.js if you haven't already.  This has been tested with v0.10.25.
2. Run 'npm install wekinator'.
3. Run 'node wek2ws.js'

## To receive the OSC messages from the browser
Add the following code snippet to your code.
```
var ws = new WebSocket( 'ws://127.0.0.1:12100' );
ws.addEventListener( 'message', function( event ) {
  var oscMessage = JSON.parse( event.data );
  // Code to parse the osc message goes here
} );
```