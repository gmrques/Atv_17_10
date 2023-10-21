#define LED_VM 11
#define LED_AZ 10
#define LED_VD 9
#define POT A0

void setup() {
  pinMode(LED_VM,OUTPUT);
  pinMode(LED_VD,OUTPUT);
  pinMode(LED_AZ,OUTPUT);
  pinMode(POT,INPUT);
  Serial.begin(9600);
}

void loop(){
  int valor = analogRead(POT);
  int tensao = (valor*5)/1023;
 
  Serial.print(tensao);
   
  
  if (tensao >= 0 && tensao < 1) {
    digitalWrite(LED_VD, LOW);
    digitalWrite(LED_VM, HIGH);
    digitalWrite(LED_AZ, LOW);
} 
  else if (tensao <= 4 && tensao >= 1) {
    digitalWrite(LED_VM, LOW);
    digitalWrite(LED_AZ, LOW);
    digitalWrite(LED_VD, HIGH);
}
  else {
    digitalWrite(LED_AZ, HIGH);
    digitalWrite(LED_VM, LOW);
    digitalWrite(LED_VD, LOW);
  }
}