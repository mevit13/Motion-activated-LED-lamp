#define Trig 12
#define Echo 13
#define Led 10
#define DIST(x) x*350.0/20000.0

void setup() {
  Serial.begin(9600);
  pinMode(Trig,OUTPUT); pinMode(Echo,INPUT); pinMode(Led,OUTPUT);
}

int t=0;
int a=0,b=0;

void loop() {
  
  trigger();
  t = pulseIn(Echo,1);
  Serial.println(DIST(t));

  if(DIST(t)<100)a=1;
  else a=0;

  /*if(a!=b)
  {
    b=a;
    if(a==0)digitalWrite(Led,LOW);
    else digitalWrite(Led,HIGH);
  }*/

  delay(100);
}

void trigger()
{
  digitalWrite(Trig,0);
  delayMicroseconds(2);
  digitalWrite(Trig,1);
   delayMicroseconds(5);
  digitalWrite(Trig,0);
}
