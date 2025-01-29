## Arduino-Light-Intensity
![image](https://github.com/user-attachments/assets/eec2377c-ec76-4e63-ba6b-e3bd137c588c)

- Pin Definitions
  - photoResistorPin: This is the analog input pin (A0) where the photoresistor is connected. It reads the light intensity.
  - greenLedPin, yellowLedPin, redLedPin: These are the digital output pins (13, 12, and 11) connected to the green, yellow, and red LEDs, respectively.

This Arduino sketch is designed to monitor light intensity and provide visual feedback through LEDs. It can dynamically adjust its thresholds in automatic mode or allow manual adjustments in manual mode. The system is user-friendly, providing real-time updates via the serial monitor and allowing for user commands to control its behavior.
