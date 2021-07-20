# infinity-cube
CircuitPython infinity cube. Control animations and colors using the free Adafruit Bluefruit app.
Build by Prof. John Gallaugher - YouTube.com/profgallaugher, Twitter: @gallaugher, Web: gallaugher.com

Build was based on original by Ruiz Bros. for Adafruit: https://learn.adafruit.com/neopixel-infinity-cube

This version includes more LEDs (72), more than the original build. If you have a different # of LEDs, be sure to change the line:
   num_leds = 72
to equal the # of LEDs in your build.

The code.py file in this repo is replacement code from the original build. Here's how it works:

Start up the LED cube and all lights will light in BLUE
- to change the default color, simply add a new color in defaultColor. You can use any of the built-in color names that you'll see toward the top of the code (name must be entered as all caps), or add it as an RGB color like this (128, 0, 0) be sure to keep parentheses around any RGB value.

- Once a user connects to the device, they can select ColorPicker to change the default color which is used for the solid color and animations associated with buttons 1, 2, and 3.

- Button 1 - performs a Comet animation from the Adafruit LED Animations library (looks like a Larson Scanner). The "tail" of the comet is set as: int(num_leds/3) + 1
- Button 2 - performs a Pulse animation - softly moving from completely black to full brightness and back again, repeating.
- Button 3 - performs a SparklePulse - twinkling on random pixels inside the cube
- Button 4 - performs a wild rainbow unicorn party with Rainbow, RainbowSparkle, and RainbowComet animations.

- The right arrow will speed up animations
- The left arrow will slow down animations
- The up arrow will stop animations and show a single light in the cube in the default color or currently selected color (although it will be reflected as multiple lights).
- The up or down arrows will move the light throughout the defined LED strip used in this build, one light space at a time.

- The Adafruit Bluefruit App (available for free for Mac, iOS, and Android) should show the name of the cube as "Cube", but this behavior is intermittent and often doesn't work. If not, you'll likely see a device named CIRCUITPY. If you want to change the name of the device that would appeare in the app (knowing it often won't appear), you can change the line: 
    advertisement.complete_name = "Cube"
but if you change the name, BE SURE that the name is 11 characters or less. As of CircuitPython 6.2, advertisement names larger than 11 characters may cause the device to not appear at all in the Bluefruit app. If the device isn't appearing on your device, close the app, turn Bluetooth off and on on the device, then open the app again. You can also try restarting the accessing device as well as the LED cube.

I'm not a native Python coder, so please share any advice on improving the code. Any enhancements will be posted here & shared with my students. And if you build this, you can tweet me a photo of your build with the hashtag #BulitWithProfG and you could win the weekly drawing for a "Make Something Awesoome" laptop sticker featuring "Happy Gear", my channel's mascot:
https://pbs.twimg.com/media/E6nXxPhXMAIPIyK?format=jpg&name=medium
