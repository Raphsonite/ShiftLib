# ShiftLib
Liturally the simplest shift register library for Arduino.

It's so darn simple. You only need 3 pins from the Arduino to control an infinite amount of digital outputs.

Here is a code snippet that you can use for your own sketches. In this case I controlled a set of 24 LED's, called "ledArray".

```
#include <ShiftLib.h>

// Constructor: ShiftLib::ShiftLib(int registerAmount, int latchPin, int clockPin, int dataPin)
ShiftLib ledArray(3, 8, 9, 10);

void setup() {
  // Heck this is a simple bit of code.
}

void loop() {
  for(int i = 0; i < 24; i++){
    ledArray.set(i, HIGH);
  }
  for(int i = 23; i >= 0; i--){
    ledArray.set(i, LOW);
  }
  delay(50);
}
```

Well. That is pretty darn simple. Have fun, bye.
