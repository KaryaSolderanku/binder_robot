//Binder Robot Arduino

#include <Servo.h>

Servo ser1;
Servo ser2;


void setup() {
  Serial.begin(115200);
  sSerial.begin(115200);
  attachServo();
  Serial.print("P");
}

void loop(){
  if(Serial.available()){
    char a = Serial.read();
    Serial.print(a);
    if(a == '0'){
      gerak(5);
      Serial.print("ok");
    }
    if(a == '1'){
      gerak(1);
    }
    if(a == '2'){
      gerak(2);
    }
    if(a == '3'){
      gerak(3);
    }
    if(a == '4'){
      gerak(4);
    }
  }
}

void gerak(int dir){
  switch(dir){
    case 1:
      ser1.write(0);
      ser2.write(180);
    break;
    case 2:
      ser1.write(180);
      ser2.write(0);
    break;
    case 3:
      ser1.write(92);
      ser2.write(180);
    break;
    case 4:
      ser1.write(0);
      ser2.write(91);
    break;
    case 5:
      ser1.write(92);
      ser2.write(91);
    break;
    default:
      ser1.write(92);
      ser2.write(91);
    break;
  }
}

void attachServo(){
  ser1.attach(8);
  ser2.attach(9);
}


void detachServo(){
  ser1.detach();
  ser2.detach();
}
