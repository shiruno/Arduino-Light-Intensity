## Arduino-Light-Intensity
![image](https://github.com/user-attachments/assets/eec2377c-ec76-4e63-ba6b-e3bd137c588c)

- Pin Definitions
  - photoResistorPin: This is the analog input pin (A0) where the photoresistor is connected. It reads the light intensity.
  - greenLedPin, yellowLedPin, redLedPin: These are the digital output pins (13, 12, and 11) connected to the green, yellow, and red LEDs, respectively.
- Functions
  - adjustThresholdsBasedOnLight(int lightIntensity): Adjusts the low and high thresholds based on the current light intensity.
  - determineActiveLed(int lightIntensity): Turns off all LEDs and determines which LED to turn on based on the current light intensity relative to the thresholds. Returns the name of the active LED.
    -  "Cloudy" for low light (0-40%)
    -  "Normal" for medium light (41-70%)
    -  "Bright Sunlight" for high light (71-100%)
  - displayStatus(int lightIntensity, String activeLed, String environment): Prints the current light intensity, mode, active LED, and environment to the serial monitor.
  - handleSerialCommands(): Listens for commands sent via the serial monitor. It can switch between automatic and manual modes, and set the low and high thresholds (only in manual mode). It provides feedback for each command.
  - turnOffAllLeds(): A helper function that turns off all LEDs by setting their pins to LOW.

This Arduino sketch is designed to monitor light intensity and provide visual feedback through LEDs. It can dynamically adjust its thresholds in automatic mode or allow manual adjustments in manual mode. The system is user-friendly, providing real-time updates via the serial monitor and allowing for user commands to control its behavior.
