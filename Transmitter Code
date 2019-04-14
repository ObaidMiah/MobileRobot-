#include <SPI.h>
#include <nRF24L01.h>
#include <RF24.h>

int two = 2; 
int three = 3; 
int valuetwo=6; 
int valuethree=6;  

RF24 radio(7, 8); // CE, CSN
const byte address[6] = "00001";

void setup() {
  radio.begin();
  radio.openWritingPipe(address);
  radio.setPALevel(RF24_PA_MIN);
  radio.stopListening();
  pinMode(two,INPUT);
  pinMode(three,INPUT);
  Serial.begin(57600);
}

void loop() {
  valuetwo = digitalRead(two); 
  valuethree = digitalRead(three);
  Serial.print(valuetwo);
  Serial.print(valuethree); 
  Serial.print('\n');
  if(valuetwo == 1 && valuethree == 1)
  { int value = 11;
  radio.write(&value,2);
  delay(1000);}
  else if(valuetwo == 1 && valuethree == 0)
  { int value = 12;
  radio.write(&value,2);
  delay(1000);}
  else if(valuetwo == 0 && valuethree == 1)
  { int value = 13;
  radio.write(&value,2);
  delay(1000);} 
  else if(valuetwo == 0 && valuethree == 0)
  { int value = 14;
  radio.write(&value,2);
  delay(1000);}
  Serial.print(value); 
  Serial.print('\n'); 
 
}
