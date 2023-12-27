# Random-New-Year-Sparkles-with-Arduino-and-Random-Numbers
 Example code for creating random New Year sparkles using Arduino and generating random numbers.
const int numLEDs = 10;
int ledPins[] = {2, 3, 4, 5, 6, 7, 8, 9, 10, 11};

void setup() {
    for (int i = 0; i < numLEDs; i++) {
        pinMode(ledPins[i], OUTPUT);
    }
}

void loop() {
    for (int i = 0; i < numLEDs; i++) {
        if (random(2) == 0) {
            digitalWrite(ledPins[i], HIGH);
        } else {
            digitalWrite(ledPins[i], LOW);
        }
    }
    delay(500);
}
