// Definieer de LED-pin
const int ledPin = 13; 

void setup() {
  pinMode(ledPin, OUTPUT); // Zet de pin als output
}

void loop() {
  digitalWrite(ledPin, HIGH); // Zet de LED aan
  delay(1000); // Wacht 1 seconde
  digitalWrite(ledPin, LOW); // Zet de LED uit
  delay(1000); // Wacht 1 seconde
}
