#rgb açik kaynak kodu arduino

int r = 3;
int g = 5; //Tanımlamalar RGB
int b = 6;

int pot1;
int pot2;//Tanımlamalar potansiyometre
int pot3;

int buzz

void setup() {

  pinMode (r, OUTPUT);
  pinMode (g, OUTPUT);
  pinMode (b, OUTPUT);   

  Serial.begin(9600);

}

void loop() {

  pot1 = analogRead (A0);
  pot2 = analogRead (A1);
  pot3 = analogRead (A2);


  pot1 = map (pot1, 0, 1023, 0, 255);
  pot2 = map (pot2, 0, 1023, 0, 255);
  pot3 = map (pot3, 0, 1023, 0, 255);

  Serial.println(pot1);

  analogWrite(r, pot1);
  analogWrite(g, pot2);
  analogWrite(b, pot3);




}
