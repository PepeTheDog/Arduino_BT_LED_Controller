#include <SoftwareSerial.h>
SoftwareSerial BTserial(2, 3);
#define led1 12

char c = ' ';

void setup(){
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  BTserial.begin(38400);
}

void loop(){
  if (BTserial.available() > 0){
    c = BTserial.read();
    Serial.println(c);
    if (c == 1)
      digitalWrite(led1, HIGH);
    else if (c == 2)
      digitalWrite(led1, LOW);
  }
}
