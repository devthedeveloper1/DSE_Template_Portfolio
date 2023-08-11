# Devarsh Omni-Wheel project
This is the Mecham Omni-Wheel robot built and completed by Devarsh Ganoorkar. I chose this project because I wanted to explore mobility, structures and electrical engineering concepts while also integrating my software experience. The biggest challenge I experienced was the quality and avaliablity of materials, I had to work with many faulty parts such as the broken LED lights, missing screws and malfunctioning IR sensors - however this was also my biggest triumph as I was able to complete the project regardless and found innovative substitues/aternatives for the missing and/or faulty parts. I was very fascinated by the electrical engineering aspect of this project as I found the arduino code to be a little bit difficult to understand without a solid background in electrical concepts. After learning about wiring and the different functions of parts such as the wifi shield, megaboard and motors - I was able to effectively visualise and understand how the arduino software integrated within the entire system. I also learned about H-diagrams, digital and analog signals/inputs and how HIGH and LOW functions can be used to bring upon rotation and varied movements through the motors. 



| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Devarsh Ganoorkar | Reedy High School | Electrical Engineering | Incoming Sophmore 

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Since I faced quite a few struggles with my original project (wheel functionality, faulty components) and a lack of time, I was unable to add any significant modifications. I did however manage to order some more IR sensors which I used to program my robot to be able to perform line tracking tasks such as following a strip of black duct tape through the use of the IR sensors. I also attempted to add a last minute modification where I could attach a possible thermal sensor/camera to identify the object with the highest heat/thermal signature and for the robot to react by moving towards the thermal signature. This was very challenging given my limited expertise in electronics and arduino, however, with help from my instructor and some online resources, I was able to create a base code (untested) that should work but since it remains untested, there is no guarantee. This was I believe my greatest challenge in the program and it is yet unknown if I managed to overcome it but I do plan to soon buy the thermal sensor and try my very best to understand it by myself. 
For your final milestone, explain the outcome of your project. However, even with all the challenges I faced, I do believe that I learned quite a lot through simply experience and technical work - before this, I had little to no experience conducting any engineering project before and even though I was not able to make the desired modifications to my project, I would say that the experience I got from this project would be invaluable. I learned about several new, relevant concepts such as H-diagrams, Arduino code, HIGH/LOW functions and more. I will say that I did make a mistake by not going through a structured and intensive engineering course before this program as it would have been far more benefical to apply previously learned information to a new project. 

# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

In my second milestone - I completed the steps I planned in my Milestone 1 video by inputting the code and setting up the ultrasonic sensors and infrared sensors. I also learned a lot about the different functions and inner workings of both the Ultrasonic sensor and IR sensors and how they take in inputs from different frequencies/wavelenghts to perform tasks such as object detection and line tracking. I did face several challenges with some more faulty components such as one of the IR sensors simply failed to respond while I had another set of screws missing to attach the ultrasonic sensor which may have interfered with the stability and accuracy of its object detection capabilities. I again overcame these challenges by using whatever materials I had around me (tape, different screws, etc) to attach the US sensor in a somewhat stable fashion which allowed the robot to work effectively. Before my final milestone - all I really need to accomplish is to gather the correct materials from my instructors and correct the faulty parts (IR sensors and wheels). Lastly, I would also prefer to finish up my modifications which I plan to be either another component of the Osyoo kit and code provided to me or my unique touch to the project (a thermal sensor with object identifcation capabilities). If possible - I would love to do both but that would have to work with my time constraints and learning curve needed to work on complex mods like the thermal sensor/imaging. 

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/NGiaRBSVVbc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


My first milestone was essentially gaining basic functionality and proper movement with the robot. I wanted to have it completely assembled and ready to move freely, however, with the missing parts, this proved to be somewhat of a challenge as the wheels were unable to fit through. I used tape, hammering and even glue to provide a temporary fix to this problem but after several launches, the wheels would evenutally fall off. This issue was major but I still persisted - I used the started code to program my robot to perform some basic rotational and forward-backward movements while also learning a lot about wiring and the functions of the different components. My plan to complete my project is to first have the main assembly finished and then I would like to start working with some of the really cool components given to me such as the Ultrasonic and IR sensors to complete complex tasks such as object detection and line tracking, which I think are very excellent projects/activities to further my understanding of electrical engineering. 

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");

#include <Servo.h>
#define speedPinR 9   //  Front Wheel PWM pin connect Model-Y M_B ENA 
#define RightMotorDirPin1  22    //Front Right Motor direction pin 1 to Model-Y M_B IN1  (K1)
#define RightMotorDirPin2  24   //Front Right Motor direction pin 2 to Model-Y M_B IN2   (K1)                                 
#define LeftMotorDirPin1  26    //Front Left Motor direction pin 1 to Model-Y M_B IN3 (K3)
#define LeftMotorDirPin2  28   //Front Left Motor direction pin 2 to Model-Y M_B IN4 (K3)
#define speedPinL 10   //  Front Wheel PWM pin connect Model-Y M_B ENB

#define speedPinRB 11   //  Rear Wheel PWM pin connect Left Model-Y M_A ENA 
#define RightMotorDirPin1B  5    //Rear Right Motor direction pin 1 to Model-Y M_A IN1 ( K1)
#define RightMotorDirPin2B 6    //Rear Right Motor direction pin 2 to Model-Y M_A IN2 ( K1) 
#define LeftMotorDirPin1B 7    //Rear Left Motor direction pin 1 to Model-Y M_A IN3  (K3)
#define LeftMotorDirPin2B 8  //Rear Left Motor direction pin 2 to Model-Y M_A IN4 (K3)
#define speedPinLB 12    //  Rear Wheel PWM pin connect Model-Y M_A ENB

#define LPT 2 // scan loop coumter

#define SERVO_PIN     13  //servo connect to D5

#define Echo_PIN    31 // Ultrasonic Echo pin connect to A5
#define Trig_PIN    30  // Ultrasonic Trig pin connect to A4

#define FAST_SPEED  160   //both sides of the motor speed
#define SPEED  120     //both sides of the motor speed
#define TURN_SPEED  120   //both sides of the motor speed
#define BACK_SPEED1  160   //back speed
#define BACK_SPEED2  90    //back speed

int leftscanval, centerscanval, rightscanval, ldiagonalscanval, rdiagonalscanval;
const int distancelimit = 30; //distance limit for obstacles in front           
const int sidedistancelimit = 30; //minimum distance in cm to obstacles at both sides (the car will allow a shorter distance sideways)
int distance;
int numcycles = 0;
const int turntime = 250; //Time the robot spends turning (miliseconds)
const int backtime = 300; //Time the robot spends turning (miliseconds)

int thereis;
Servo head;
/*motor control*/
void go_Advance()  //Forward
{
FR_fwd();
FL_fwd();
RR_fwd();
RL_fwd();
}
void go_Left()  //Turn left
{
FR_fwd();
FL_bck();
RR_fwd();
RL_bck();
}
void go_Right()  //Turn right
{
FR_bck();
FL_fwd();
RR_bck();
RL_fwd();
}
void go_Back()  //Reverse
{
FR_bck();
FL_bck();
RR_bck();
RL_bck();
}
 
 

void stop_Stop()    //Stop
{
  digitalWrite(RightMotorDirPin1, LOW);
  digitalWrite(RightMotorDirPin2,LOW);
  digitalWrite(LeftMotorDirPin1,LOW);
  digitalWrite(LeftMotorDirPin2,LOW);
  digitalWrite(RightMotorDirPin1B, LOW);
  digitalWrite(RightMotorDirPin2B,LOW);
  digitalWrite(LeftMotorDirPin1B,LOW);
  digitalWrite(LeftMotorDirPin2B,LOW);
  set_Motorspeed(0,0,0,0);
}

/*set motor speed */
void set_Motorspeed(int leftFront,int rightFront,int leftBack,int rightBack)
{
 analogWrite(speedPinL,leftFront); 
 analogWrite(speedPinR,rightFront); 
 analogWrite(speedPinLB,leftBack);  
 analogWrite(speedPinRB,rightBack);

}

void FR_fwd()  //front-right wheel forward turn
{
  digitalWrite(RightMotorDirPin1,HIGH);
  digitalWrite(RightMotorDirPin2,LOW); 
}
void FR_bck() // front-right wheel backward turn
{
  digitalWrite(RightMotorDirPin1,LOW);
  digitalWrite(RightMotorDirPin2,HIGH); 
}
void FL_fwd() // front-left wheel forward turn
{
  digitalWrite(LeftMotorDirPin1,HIGH);
  digitalWrite(LeftMotorDirPin2,LOW);
}
void FL_bck() // front-left wheel backward turn
{
  digitalWrite(LeftMotorDirPin1,LOW);
  digitalWrite(LeftMotorDirPin2,HIGH);
}

void RR_fwd()  //rear-right wheel forward turn
{
  digitalWrite(RightMotorDirPin1B,HIGH);
  digitalWrite(RightMotorDirPin2B,LOW); 
}
void RR_bck()  //rear-right wheel backward turn
{
  digitalWrite(RightMotorDirPin1B,LOW);
  digitalWrite(RightMotorDirPin2B,HIGH); 
}
void RL_fwd()  //rear-left wheel forward turn
{
  digitalWrite(LeftMotorDirPin1B,HIGH);
  digitalWrite(LeftMotorDirPin2B,LOW);
}
void RL_bck()    //rear-left wheel backward turn
{
  digitalWrite(LeftMotorDirPin1B,LOW);
  digitalWrite(LeftMotorDirPin2B,HIGH);
}

/*detection of ultrasonic distance*/
int watch(){
  long echo_distance;
  digitalWrite(Trig_PIN,LOW);
  delayMicroseconds(5);                                                                              
  digitalWrite(Trig_PIN,HIGH);
  delayMicroseconds(15);
  digitalWrite(Trig_PIN,LOW);
  echo_distance=pulseIn(Echo_PIN,HIGH);
  echo_distance=echo_distance*0.01657; //how far away is the object in cm
 //Serial.println((int)echo_distance);
  return round(echo_distance);
}
//Meassures distances to the right, left, front, left diagonal, right diagonal and asign them in cm to the variables rightscanval, 
//leftscanval, centerscanval, ldiagonalscanval and rdiagonalscanval (there are 5 points for distance testing)
String watchsurrounding(){
/*  obstacle_status is a binary integer, its last 5 digits stands for if there is any obstacles in 5 directions,
 *   for example B101000 last 5 digits is 01000, which stands for Left front has obstacle, B100111 means front, right front and right ha
 */
 
int obstacle_status =B100000;
  centerscanval = watch();
  if(centerscanval<distancelimit){
    stop_Stop();
    
    obstacle_status  =obstacle_status | B100;
    }
  head.write(120);
  delay(100);
  ldiagonalscanval = watch();
  if(ldiagonalscanval<distancelimit){
    stop_Stop();
    
     obstacle_status  =obstacle_status | B1000;
    }
  head.write(170); //Didn't use 180 degrees because my servo is not able to take this angle
  delay(300);
  leftscanval = watch();
  if(leftscanval<sidedistancelimit){
    stop_Stop();
    
     obstacle_status  =obstacle_status | B10000;
    }

  head.write(90); //use 90 degrees if you are moving your servo through the whole 180 degrees
  delay(100);
  centerscanval = watch();
  if(centerscanval<distancelimit){
    stop_Stop();
    
    obstacle_status  =obstacle_status | B100;
    }
  head.write(40);
  delay(100);
  rdiagonalscanval = watch();
  if(rdiagonalscanval<distancelimit){
    stop_Stop();
    
    obstacle_status  =obstacle_status | B10;
    }
  head.write(0);
  delay(100);
  rightscanval = watch();
  if(rightscanval<sidedistancelimit){
    stop_Stop();
    
    obstacle_status  =obstacle_status | 1;
    }
  head.write(90); //Finish looking around (look forward again)
  delay(300);
   String obstacle_str= String(obstacle_status,BIN);
  obstacle_str= obstacle_str.substring(1,6);
  
  return obstacle_str; //return 5-character string standing for 5 direction obstacle status
}

void auto_avoidance(){

  ++numcycles;
  if(numcycles>=LPT){ //Watch if something is around every LPT loops while moving forward 
     stop_Stop();
    String obstacle_sign=watchsurrounding(); // 5 digits of obstacle_sign binary value means the 5 direction obstacle status
      Serial.print("begin str=");
        Serial.println(obstacle_sign);
                    if( obstacle_sign=="10000"){
     Serial.println("SLIT right");
          set_Motorspeed(FAST_SPEED,SPEED,FAST_SPEED,SPEED);
     go_Advance();
 
      delay(turntime);
      stop_Stop();
    }
        else    if( obstacle_sign=="00001"  ){
     Serial.println("SLIT LEFT");
       set_Motorspeed(SPEED,FAST_SPEED,SPEED,FAST_SPEED);
      go_Advance();
  
      delay(turntime);
      stop_Stop();
    }
    else if( obstacle_sign=="11100" || obstacle_sign=="01000" || obstacle_sign=="11000"  || obstacle_sign=="10100"  || obstacle_sign=="01100" ||obstacle_sign=="00100"  ||obstacle_sign=="01000" ){
     Serial.println("hand right");
	    go_Right();
      set_Motorspeed(TURN_SPEED,TURN_SPEED,TURN_SPEED,TURN_SPEED);
      delay(turntime);
      stop_Stop();
    } 
    else if( obstacle_sign=="00010" || obstacle_sign=="00111" || obstacle_sign=="00011"  || obstacle_sign=="00101" || obstacle_sign=="00110" || obstacle_sign=="01010" ){
    Serial.println("hand left");
     go_Left();//Turn left
     set_Motorspeed(TURN_SPEED,TURN_SPEED,TURN_SPEED,TURN_SPEED);
      delay(turntime);
      stop_Stop();
    }
 
    else if(  obstacle_sign=="01111" ||  obstacle_sign=="10111" || obstacle_sign=="11111"  ){
    Serial.println("hand back left");
	  go_Back();
		set_Motorspeed( BACK_SPEED1,BACK_SPEED2,BACK_SPEED1,BACK_SPEED2);
       delay(backtime);
          stop_Stop();
        } 
         else if( obstacle_sign=="11011"  ||    obstacle_sign=="11101"  ||  obstacle_sign=="11110"  || obstacle_sign=="01110"  ){
    Serial.println("hand back right");
   go_Back();
    set_Motorspeed(BACK_SPEED2,BACK_SPEED1,BACK_SPEED2,BACK_SPEED1);
       delay(backtime);
          stop_Stop();
        }    
  
        else Serial.println("no handle");
    numcycles=0; //Restart count of cycles
  } else {
     set_Motorspeed(SPEED,SPEED,SPEED,SPEED);
     go_Advance();  // if nothing is wrong go forward using go() function above.
        delay(backtime);
          stop_Stop();
  }
  
  //else  Serial.println(numcycles);
  
  distance = watch(); // use the watch() function to see if anything is ahead (when the robot is just moving forward and not looking around it will test the distance in front)
  if (distance<distancelimit){ // The robot will just stop if it is completely sure there's an obstacle ahead (must test 25 times) (needed to ignore ultrasonic sensor's false signals)
 Serial.println("final go back");
	go_Back();
  set_Motorspeed(BACK_SPEED1,BACK_SPEED2,BACK_SPEED1,BACK_SPEED2);
  delay(backtime);
      ++thereis;}
  if (distance>distancelimit){
      thereis=0;} //Count is restarted
  if (thereis > 25){
  Serial.println("final stop");
    stop_Stop(); // Since something is ahead, stop moving.
    thereis=0;
  }
}

void setup() {
  /*setup L298N pin mode*/
  pinMode(RightMotorDirPin1, OUTPUT); 
  pinMode(RightMotorDirPin2, OUTPUT); 
  pinMode(speedPinL, OUTPUT);  
 
  pinMode(LeftMotorDirPin1, OUTPUT);
  pinMode(LeftMotorDirPin2, OUTPUT); 
  pinMode(speedPinR, OUTPUT);
  pinMode(RightMotorDirPin1B, OUTPUT); 
  pinMode(RightMotorDirPin2B, OUTPUT); 
  pinMode(speedPinLB, OUTPUT);  
 
  pinMode(LeftMotorDirPin1B, OUTPUT);
  pinMode(LeftMotorDirPin2B, OUTPUT); 
  pinMode(speedPinRB, OUTPUT);
  stop_Stop();//stop move
  /*init HC-SR04*/
  pinMode(Trig_PIN, OUTPUT); 
  pinMode(Echo_PIN,INPUT); 
  /*init buzzer*/
 
  digitalWrite(Trig_PIN,LOW);
  /*init servo*/
  head.attach(SERVO_PIN); 
    head.write(0);
   delay(1000);
     head.write(170);
   delay(1000);
  head.write(90);
   delay(8000);
  
  Serial.begin(9600);
 
 
 
  stop_Stop();//Stop
 
}

void loop() {
auto_avoidance();
// Serial.println( watchsurrounding());
}
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials (List of main tools/equipment used)
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Engineering kit | A general kit for engineering tools like solders, screwdrivers, pliers, etc | $28 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Soldering-Iron-Kit-Temperature-Desoldering/dp/B07Q2B4ZY9/ref=asc_df_B07Q2B4ZY9/?tag=hyprod-20&linkCode=df0&hvadid=343209938057&hvpos=&hvnetw=g&hvrand=9711908616551175950&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1026836&hvtargid=pla-739851839715&psc=1&tag=&ref=&adgrpid=68249717199&hvpone=&hvptwo=&hvadid=343209938057&hvpos=&hvnetw=g&hvrand=9711908616551175950&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1026836&hvtargid=pla-739851839715)https://www.amazon.com/Soldering-Iron-Kit-Temperature-Desoldering/dp/B07Q2B4ZY9/ref=asc_df_B07Q2B4ZY9/?tag=hyprod-20&linkCode=df0&hvadid=343209938057&hvpos=&hvnetw=g&hvrand=9711908616551175950&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1026836&hvtargid=pla-739851839715&psc=1&tag=&ref=&adgrpid=68249717199&hvpone=&hvptwo=&hvadid=343209938057&hvpos=&hvnetw=g&hvrand=9711908616551175950&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1026836&hvtargid=pla-739851839715"> Link </a> |
| Wifi Shield | proccessing unit for code and motors | $26 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/)"> Link </a> |
| Ultrasonic sensors | Used for object detection and possible avoidance programs | $5 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.mouser.com/ProductDetail/SparkFun/SEN-15569?qs=P1JMDcb91o46Sr4O2RLYiA%3D%3D&mgh=1&gclid=CjwKCAjw8symBhAqEiwAaTA__DmNyCNNDa_fu7QRWrp8iziGg2rnpYlMuK4i06CQCwpmb_nPz7vm8hoCN7MQAvD_BwE)https://www.mouser.com/ProductDetail/SparkFun/SEN-15569?qs=P1JMDcb91o46Sr4O2RLYiA%3D%3D&mgh=1&gclid=CjwKCAjw8symBhAqEiwAaTA__DmNyCNNDa_fu7QRWrp8iziGg2rnpYlMuK4i06CQCwpmb_nPz7vm8hoCN7MQAvD_BwE"> Link </a> |
| IR sensors | used to detect different frequencies and wavelenghts and input them along with code to react (depending on what reaction was intended when detecting different inputs) | $10 | <a href="  https://www.amazon.com/Gikfun-avoidance-Reflective-Photoelectric-Intensity/dp/B07FJLMLVZ/ref=asc_df_B07FJLMLVZ/?tag=hyprod-20&linkCode=df0&hvadid=242021018855&hvpos=&hvnetw=g&hvrand=13900884704753398350&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1026836&hvtargid=pla-525961642959&psc=1 "> Link </a> |


