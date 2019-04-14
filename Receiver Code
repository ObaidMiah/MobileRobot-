#include <SPI.h>
#include <nRF24L01.h>
#include <RF24.h>

const int rightMotor = 5;
const int leftMotor = 6;

RF24 radio(7, 8); // CE, CSN
const byte address[6] = "00001";

void setup() {
  Serial.begin(9600);
  radio.begin();
  radio.openReadingPipe(0, address);
  radio.setPALevel(RF24_PA_MIN);
  radio.startListening();
  pinMode(rightMotor, OUTPUT);
  pinMode(leftMotor, OUTPUT); 
}
void loop() {
  
  if (radio.available()) {
    int value; 
    radio.read(&value,2);
    Serial.println(value);
  //value = 11; 
  //value = 12; 
  //value = 13; 
  //value = 14 
  if(value == 11)
  {analogWrite(rightMotor,255);
  analogWrite(leftMotor,255);}
  else if(value == 12)
  {analogWrite(rightMotor,255);
  analogWrite(leftMotor,0);}
  else if(value == 13)
  {analogWrite(rightMotor,0);
  analogWrite(leftMotor,255);} 
  else if(value == 14)
  {analogWrite(rightMotor,0);
  analogWrite(leftMotor,0);}
  }
  
}
