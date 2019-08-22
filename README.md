# Launchpad
Javascript Library for Launchpad

This is a simple javascript library you can include to detect and connect with a launchpad and use it as a secondary display device.

usage : 
- include the script 
```javascript
var LP = new LaunchPad ({
	onMidiNoteIn:midiNoteIn,
	onConnect:midiConnected,
	onFrameRender:renderFrame
});

function midiNoteIn (ev)
 {
 // handle EV as you need for input
 console.log (ev);
 }
 
function midiConnected () {
console.log ("midi Connected");
console.log (LP);	
}
 
function renderFrame (delta)
{
// this function would handle rendering new data.
// velocity is the color, but you can get a value by red and green
LP.clearScreen(0);
vel = LP.rgColor (red,green);
LP.setPixel (x,y,vel);
}
```
