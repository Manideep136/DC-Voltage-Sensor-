# DC-Voltage-Sensor

# High DC Voltage Sensor PCB Using KiCad

## 📌 Project Overview

This project focuses on designing a **High DC Voltage Sensor PCB** using KiCad. The circuit is intended to measure a DC voltage higher than the input range of a microcontroller or measurement device by scaling the voltage to a suitable level.

A resistor voltage divider is a common method for reducing a high DC voltage to a lower proportional voltage. The scaled output can then be measured using a suitable analog-to-digital converter (ADC), microcontroller, or measurement instrument.

This project demonstrates voltage sensing, resistor selection, schematic design, footprint assignment, and PCB layout using KiCad.

## 🎯 Objectives

- Understand the principle of high DC voltage measurement.
- Learn how a resistor voltage divider works.
- Design a DC voltage sensing circuit.
- Create the schematic using KiCad.
- Assign suitable footprints to electronic components.
- Design and route the PCB.
- Perform Electrical Rules Check (ERC) and Design Rules Check (DRC).
- Inspect the completed PCB using KiCad's 3D Viewer.

## ⚙️ Working Principle

The sensor scales the input DC voltage using a resistor network.

The voltage divider consists of two resistors connected in series across the input voltage. The output is measured across the lower resistor.

The voltage divider equation is:

```text
Vout = Vin × R2 / (R1 + R2)
```

Where:

- `Vin` = Input DC voltage.
- `Vout` = Scaled output voltage.
- `R1` = Upper resistor of the voltage divider.
- `R2` = Lower resistor of the voltage divider.

When a high DC voltage is applied, the resistor network reduces it to a lower voltage proportional to the input.

The output can be connected to a measurement circuit, provided the output voltage remains within the permitted input range of that circuit.

**Note:** The actual resistor values, maximum input voltage, output range, and protection components must match the circuit shown in the reference design.

## 🔌 Block Diagram

```text
     High DC Voltage Input
              |
              v
      Resistor Divider
              |
              v
      Scaled DC Voltage
              |
              v
      Measurement Circuit
              |
              v
       Voltage Reading
```

## 🧩 Components Used

The final bill of materials depends on the actual schematic.

| Component | Function |
|---|---|
| R1 | Upper voltage-divider resistor |
| R2 | Lower voltage-divider resistor |
| Input connector | Connects the DC voltage source |
| Output connector | Provides the scaled voltage output |
| Protection components | Help protect the measurement circuit, if included |
| Filter capacitor | Reduces noise, if included |

Additional resistors, capacitors, diodes, or active components may be required depending on the reference circuit.

## 🖥️ PCB Design Using KiCad

The PCB design process includes:

1. Creating a new KiCad project.
2. Drawing the high DC voltage sensor schematic.
3. Adding the required components.
4. Connecting the voltage-divider network.
5. Assigning suitable footprints.
6. Updating the PCB from the schematic.
7. Arranging the components on the PCB.
8. Routing the copper tracks.
9. Running ERC in the schematic editor.
10. Running DRC in the PCB editor.
11. Inspecting the final PCB using the 3D Viewer.

## 📁 Project Structure

```text
High-DC-Voltage-Sensor/
├── High-DC-Voltage-Sensor.kicad_pro
├── High-DC-Voltage-Sensor.kicad_sch
├── High-DC-Voltage-Sensor.kicad_pcb
├── README.md
└── Images/
    ├── schematic.png
    ├── pcb_layout.png
    └── 3d_view.png
```

## 📐 PCB Design Considerations

- Select resistor values according to the intended input voltage range.
- Check the voltage rating and power dissipation of each resistor.
- Consider using multiple series resistors when a single resistor cannot safely withstand the voltage.
- Ensure the scaled output never exceeds the connected ADC or instrument's input limits.
- Add suitable input protection where required by the design.
- Choose connectors rated for the intended voltage and current.
- Maintain suitable PCB creepage and clearance distances.
- Use suitable track widths and appropriate PCB materials for the voltage involved.

## 🧪 Testing Procedure

1. Inspect the PCB for solder bridges and incorrect connections.
2. Verify resistor values and component orientation.
3. Check the input and output connector pin assignments.
4. Run ERC and DRC in KiCad.
5. Begin testing with a safe, current-limited, low-voltage DC source.
6. Measure the input voltage with a suitable multimeter.
7. Measure the divider output voltage.
8. Compare the measured output with the calculated voltage-divider output.
9. Check the scaling accuracy before connecting any microcontroller or ADC.

Testing at higher voltages should only be performed with properly rated equipment and a design that has been reviewed for electrical safety.

## ⚠️ Safety Precautions

**High DC voltage can cause serious injury or death.**

- Do not touch the circuit while it is energized.
- Do not connect an unverified high-voltage circuit directly to a microcontroller.
- Check resistor voltage ratings, power ratings, insulation, and PCB spacing.
- Use appropriate fusing, enclosures, and protection.
- Discharge capacitors safely before handling the circuit.
- Do not assume that a voltage divider provides electrical isolation.
- Test with low voltage first and obtain qualified review before high-voltage operation.

## 🚀 Future Improvements

- Add an LCD or OLED voltage display.
- Interface the sensor with an Arduino or other suitable microcontroller.
- Add overvoltage protection.
- Improve measurement accuracy through calibration.
- Add filtering to reduce noise.
- Include a connector for data logging.
- Develop a digital voltage monitoring system.

## 📚 Learning Outcomes

Through this project, I learned:

- Principles of DC voltage measurement.
- Voltage-divider calculations.
- Resistor voltage and power ratings.
- Schematic design using KiCad.
- Footprint assignment.
- PCB component placement and routing.
- ERC and DRC verification.
- Basic PCB safety considerations.
- Testing and calibration of voltage-sensing circuits.

## 🛠️ Software Used

**KiCad 9.0**



This project is intended for educational and learning purposes. The circuit must be verified against the actual schematic and tested safely before practical use.
