---
title: "Arduino Traffic Light"
date: 2025-09-28
---

I built a simple traffic light using an Arduino and a traffic light module with 3 LEDs (red, yellow, green).  
The program cycles through the lights in the same order as a real traffic light.

```cpp
// LED pins on the module
const int redPin = 8;    // Red
const int yellowPin = 9; // Yellow
const int greenPin = 10; // Green

void setup() {
  // Set pins as outputs
  pinMode(redPin, OUTPUT);
  pinMode(yellowPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
}

void loop() {
  // 1. Red on
  digitalWrite(redPin, HIGH);
  digitalWrite(yellowPin, LOW);
  digitalWrite(greenPin, LOW);
  delay(5000); // Red for 5 seconds

  // 2. Red and yellow on
  digitalWrite(redPin, HIGH);
  digitalWrite(yellowPin, HIGH);
  digitalWrite(greenPin, LOW);
  delay(2000); // Red + yellow for 2 seconds

  // 3. Green on
  digitalWrite(redPin, LOW);
  digitalWrite(yellowPin, LOW);
  digitalWrite(greenPin, HIGH);
  delay(5000); // Green for 5 seconds

  // 4. Yellow on
  digitalWrite(redPin, LOW);
  digitalWrite(yellowPin, HIGH);
  digitalWrite(greenPin, LOW);
  delay(2000); // Yellow for 2 seconds
}
