# Lab3CProgramming2

void setup() {
  // put your setup code here, to run once:

  pinMode(4, OUTPUT);

  pinMode(A6, INPUT);
  int lightLevel = analogRead(A6);
  Serial.begin(9600);
  Serial.println(lightLevel);
  

  if (lightLevel < 100) {
    Serial.println("It’s really dark!");
    digitalWrite(4, HIGH);
  } else if (lightLevel < 200) {
    Serial.println("It’s dim in here");
  } else if (lightLevel < 700) {
    Serial.println("It’s a little bright");
  } else {
    Serial.println("It’s really bright!");
  }


}



void loop() {
  // put your main code here, to run repeatedly:

}
