# 6Motors
![image](https://user-images.githubusercontent.com/86917834/127994150-4e92b88d-13b2-4f3c-97d2-0309a610abc0.png)


#include <Servo.h>
int i = 0;
int position = 0;
int j = 0;
Servo servo_11; //M1
Servo servo_10;//M2
Servo servo_9; //M3
void setup(){
  servo_11.attach(11, 500, 2500);
  servo_10.attach(10, 500, 2500);
  servo_9.attach(9, 500, 2500);
}
void loop()
{
  //M1
  
  position = 0;
  for (position = 1; position <= 89; position += 1) {
    servo_11.write(position);
    delay(20); // Wait for 20 millisecond(s)
  }
  for (j = 89; j >= 1; j -= 1) {
    servo_11.write(position);}
  //M2
  position = 0;
  for (position = 1; position <= 179; position += 1) {
    servo_10.write(position);
    delay(20); // Wait for 20 millisecond(s)
  }
  for (j = 179; j >= 1; j -= 1) {
    servo_10.write(position);}
  //M3
  position = 0;
  for (position = 1; position <= 359; position += 1) {
    servo_9.write(position);
    delay(20); // Wait for 20 millisecond(s)
  }
for (j = 359; j >= 1; j -= 1) {
servo_9.write(position);}
  }
