# PIR-Sensor-
# task 1 
# design and pregaming of  digital and along sensor

# in this task used sensor called PIR motion sensor and its digetal sensor 
# I've used tinkercad Programm to complete this task


![لقطة شاشة 2025-01-18 150539](https://github.com/user-attachments/assets/28a0f570-6690-4c16-9dab-40fba7ebea61)


# code 
int sensorState = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  // read the state of the sensor/digital input
  sensorState = digitalRead(2);
  // check if sensor pin is HIGH. if it is, set the
  // LED on.
  if (sensorState == HIGH) {
    digitalWrite(LED_BUILTIN, HIGH);
    Serial.println("Sensor activated!");
  } else {
    digitalWrite(LED_BUILTIN, LOW);
  }
  delay(10); // Delay a little bit to improve simulation performance
}
