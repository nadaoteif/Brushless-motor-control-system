
# Design Brushless motor control system 
## Overview:

These tasks is completed by [Nada Oteif](https://sa.linkedin.com/in/nadaoteif) as a part of [Smart Method](https://s-m.com.sa/en/index.html) for Summer training in 2022 at Electronics and Power track.

## Description:

### Brushless Motor simulation

![Brushless](Brushless.mp4)

[Click here to view simulation in Tinkercad](https://www.tinkercad.com/things/k81S1oNHR6e)

### Code 
``` c++ 
int btn = 0;
int psio = 0;
int data = 0;
int pinA = 7;
int pinB = 8;
int pwm = 9;
void setup() {
  pinMode(2, INPUT);
  pinMode(7, OUTPUT);
  pinMode(8, OUTPUT);
}
void loop() {
  btn = digitalRead(2);
  if(btn == LOW){
    digitalWrite(pinA, LOW);
    digitalWrite(pinB, HIGH);
    data = analogRead(psio);
    analogWrite(pwm, data);
    delay(10);  
  }
  else if (btn == HIGH){
    digitalWrite(pinA, HIGH);
    digitalWrite(pinB, LOW);
    data = analogRead(psio);
    analogWrite(pwm, data);
    delay(10);  
  }
  delay(5);
}
```
