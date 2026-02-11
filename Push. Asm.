#include <LiquidCrystal.h>

// Define pins for LM35 sensor
const int tempPin = A0;

// Define pins for LCD display (if using)
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  // Initialize serial communication
  Serial.begin(9600);

  // Initialize LCD display (if using)
  lcd.begin(16, 2);
  lcd.print("Temperature:");
}

void loop() {
  // Read temperature from LM35 sensor
  int tempValue = analogRead(tempPin);
  float temperature = (tempValue * 5.0 * 100.0) / 1024.0;

  // Display temperature on serial monitor
  Serial.print("Temperature: ");
  Serial.print(temperature);
  Serial.println("°C");

  // Display temperature on LCD display (if using)
  lcd.setCursor(0, 1);
  lcd.print(temperature);
  lcd.print("°C");

  // Delay for 1 second
  delay(1000);
}
