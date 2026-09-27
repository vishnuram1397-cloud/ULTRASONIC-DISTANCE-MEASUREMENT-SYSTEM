# ULTRASONIC-DISTANCE-MEASUREMENT-SYSTEM........
int trigPin = 9;
int echoPin = 10;
long duration;
float distance;
void setup() {
  pinMode(trigPin,OUTPUT);
  pinMode(echoPin,INPUT);
  Serial.begin(9600);
  
}

void loop() {
  digitalWrite(trigPin,HIGH);
  delay(1000);
  digitalWrite(trigPin,LOW);
  duration = pulseIn(echoPin,HIGH);
  distance = duration*0.034/2;
  Serial.print("Distance:");
  Serial.println(distance);

}
