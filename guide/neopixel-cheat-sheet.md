---
NeoPixel Library Cheat Sheet
---

Include and Defines
------------
```
#include <Adafruit_NeoPixel.h>
#define LEDPIN 12 // connect the Data from the strip to this pin on the Arduino

#define NUMBER_PIXELS 12 // the number of pixels in your LED strip
Adafruit_NeoPixel strip = Adafruit_NeoPixel(NUMBER_PIXELS, LEDPIN, NEO_GRB + NEO_KHZ800);
```

Setup
------------
```void setup() {
  strip.begin();
  strip.show();
}```

Setting Strip Color
```strip.setPixelColor(i, red, green, blue);```

where:
i is the index (0 to 11 for a 12 pixel strip)
<span style="color:red">red<span> is the value of the red LED (0=off, 255=brightest value)
green is the value of the green LED (0=off, 255=brightest value)
blue is the value of the blue LED (0=off, 255=brightest value)

```for (i=0; i <= strip.numPixels();; i++) {
      strip.setPixelColor(i, 100, 100, 100)
   }
```

To Find Out More
[Neopixel Guide](https://learn.adafruit.com/downloads/pdf/adafruit-neopixel-uberguide.pdf) 39 page PDF