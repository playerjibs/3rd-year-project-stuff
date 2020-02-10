#include <SoftwareSerial.h>
#include <Wire.h>
#include <Adafruit_MMA8451.h>
#include <Adafruit_Sensor.h>
SoftwareSerial receive_data =  SoftwareSerial(2, 3);
void setup() {
  // put your setup code here, to run once:
  receive_data.begin(38400);
Serial.begin(38400);

}

void loop() {
  // put your main code here, to run repeatedly:
  String messagee;
 if (receive_data.available()>0)
  {
    Serial.print(receive_data.read());
    
   
  }
  
  delay(10);
  
}
