### **Digital Thermometer Using 8051 and ADC0808**
## Introduction
This project demonstrates the design and implementation of a digital thermometer using an 8051 microcontroller and an ADC0808 analog-to-digital converter. The system measures temperature using an LM35 temperature sensor and displays the result on a 16x2 LCD screen.

## Features
- Measures and displays real-time temperature
- Converts analog temperature values to digital using ADC0808
- LCD interface for clear temperature readings
- Timer-based ADC clock generation

## Components Used
- 8051 Microcontroller
- ADC0808 (Analog-to-Digital Converter)
- LM35 Temperature Sensor
- 16x2 LCD Display

## Miscellaneous components: 
- Resistors, Capacitors, Power supply, Connecting wires

## Circuit Connections:
#### LM35 Temperature Sensor
- VCC → 5V
- GND → Ground
- VOUT → IN0 of ADC0808
#### ADC0808
- VCC & GND → 5V & Ground
- VREF(+) & VREF(-) → 2.56V & Ground
- IN0-IN7 → Analog input channels (IN0 connected to LM35)
- Control Pins: ALE, START, EOC, OE → Connected to 8051
- Address Pins: ADDR A, B, C → For channel selection
- Data Output (D0-D7) → Connected to 8051 port (e.g., P1.0-P1.7)
#### LCD Display
- RS, RW, EN → Connected to P2.5, P2.6, and P2.7
- Data Pins (D0-D7) → Connected to P3.0 to P3.7

## Working Principle
- Temperature Sensing: The LM35 sensor converts ambient temperature into an analog voltage.
- Analog to Digital Conversion: The ADC0808 converts this voltage into an 8-bit digital value.
- Data Processing and Display: The 8051 microcontroller reads the digital value, processes it, and displays the temperature on the LCD.

## Software Implementation
- Programming Language: C
- Compiler: Keil µVision 4
- Simulation Tool: Proteus 8.0

## Future Enhancements
- Data logging for temperature history
- Wireless transmission using IoT integration
- Temperature alerts for high/low thresholds

## Conclusion
This project successfully demonstrates how an 8051 microcontroller can interface with an ADC0808 to build a digital thermometer. The system accurately reads and displays temperature in real-time.

