---
title: "ESP32 Blinking LED"
date: 2025-10-04
---

I built a small LED blinker using an ESP32 and a single external LED. The program makes the LED turn on and off repeatedly.

```cpp
const int ledPin = 5;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH); // LED on
  delay(500);
  digitalWrite(ledPin, LOW);  // LED off
  delay(500);
}
