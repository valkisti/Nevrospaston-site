# Embedded Programming

## Programming and Debugging
[Programming Recitation](https://fabacademy.org/2026/recitation/debugging/)

Notes on Lecture
*The old version and new version of Arduino works well but some version in between like Arduino 2.0 and 2.1 are buggy

## Embedded Programming

**Harvard Architecture**

CISC: COMPLEX CONSTRUCTION SET , PROCESSORS THAT CAN RUN MANY INSTRUCTIONS
RISC: run a smaller instruction set, but they run it very quickly ->usually use this 

Use Harvard Architecture Risk Microcontrollers

Thonny: Python fro Embedded

[Embedded programming Practical](https://hackmd.io/@danimateos/rknAq7cFJe)

[How to Use an Arduino](https://www.sciencebuddies.org/science-fair-projects/references/how-to-use-an-arduino?ytid=XrJ_zLWFGFw&ytsrc=description)

### Micropython

#### Libraries
* **Machine**: It communicates directly with the hardware(pins, PWM, ADV, 12C, SPI)

```
from machine import Pin, PWM, ADC
```

* **Time**: Controls delays and timestamps

```
import time

time.sleep(0.5)     # Stops for 0.5 seconds(500 ms)
time.sleep_ms(500)  # Stops for 500 milliseconds
time.ticks_ms()     # Counts milliseconds from the start of the program
```

* **Math**: For math equations
```
import math
```
### Machien Language Arduino/Micropython
| Λειτουργία | Arduino C++ | MicroPython | Τι κάνει στην πράξη |
| :--- | :--- | :--- | :--- |
| **Ψηφιακή Έξοδος** | `pinMode(15, OUTPUT);`<br>`digitalWrite(15, HIGH);` | `led = Pin(15, Pin.OUT)`<br>`led.value(1)` *(ή `led.on()`)* | Δίνει `3.3V` (`1`) ή `0V` (`0`) στο pin 15. |
| **Ψηφιακή Είσοδος** | `pinMode(14, INPUT_PULLUP);`<br>`digitalRead(14)` | `btn = Pin(14, Pin.IN, Pin.PULL_UP)`<br>`btn.value()` | Διαβάζει `1` (ελεύθερο) ή `0` (πατημένο προς GND). |
| **PWM (Ένταση / Servo)** | `analogWrite(15, 128);` | `pwm = PWM(Pin(15))`<br>`pwm.freq(1000)`<br>`pwm.duty_u16(32768)` | Ρυθμίζει την ένταση σε 16-bit (`0` έως `65535`). |
| **Αναλογική Είσοδος** | `analogRead(26)` *(0–1023)* | `pot = ADC(Pin(26))`<br>`pot.read_u16()` *(0–65535)* | Διαβάζει τάση (`0V–3.3V`) σε pins που υποστηρίζουν ADC (`GP26–28`). |

### Functions

```
led.toggle()   # Changes the state(if it was 1 it goes to 0, viseversa)