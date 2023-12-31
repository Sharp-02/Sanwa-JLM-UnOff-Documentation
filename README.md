# Sanwa JLM Unofficial Documentation
Non-affiliated documentation, deconstruction, and partial reverse engineering of the Sanwa JLM (Joystick Lever Magnetic).

### Electrical Specifications:

Manufacturer Specifications:
* Recommended Source Voltage: 5V
* Voltage Swing: +/- 1.5V from Center
* Center Voltage Drift: 0.3V

Pinout:
* Red: V Supply (min 3.1V, max tested 5V)
* Green: Y Axis
* Blue: X Axis
* White: Push-In "Switch"
* Black: Ground

Measured at 5V:
* Center Voltage: 2.5V
* Current Draw: 50mA
* Voltage Range: +/- 1V From Center 
    * (1.53V - 3.44V Y)
* Circularity Error (RMS): 9.3%

Switch Characteristics:
* Operated by pressing lever in
* Minimum Supply Voltage: 1.6V
* Output Standing Voltage: Matches V Supply
* Output Activated Voltage: 0.03V
* Switch Activation (Fall) Time: 80ns
* Switch Deactivation (Rise) Time: 360ns
* Note: Switch can only be acticated around +/- 7 degrees from center

----------

## Documentation Objectives:

### Physical Documentation
* Pictures and dimensions of joystick components
   * Shaft Diameter
   * Top Hole Diameter
   * Dust Cover ID & OD
* Physical throw max angle
* Physical throw deadzone
* Pivot height relative to top of mounting panel
* Lever thickness

### Electrical Documentation
* Input voltage (2.5V, 3.3V, 5V, 7V)
     * corresponding current
     * resulting maximum, minimum, and center voltages
* Connector Type
* Push-in normal and activated conditions
* Push in effects on voltage


### Signal Documentation
* Angle at max/min voltage
* Signal center deadzone (if any)
* Sensitivity (per axis direction)
* Analog output step resolution
    * Does resolution change with angle?    
* Tables relating direction and sensitivity
* Standing Voltage Noise
* measured with no signal conditioning and with simple 3x gain


### Other
Snapback:
* Return Time
* % Overshoot
* Settle Time

Calibration Gates:
* Max angle octagonal
    * 1.0 and 0.707 inputs 
* Half angle square
    * 0.5 corner inputs (tests axis codependence)
* Half angle diamond
    * 0.5 cardinal inputs 
* Quarter angle diamond
    * 0.25 cardinal inputs
* 10% diamond
    * 0.1 cardinal inputs (tests near zero sensitivity)
* 5% diamond
    * 0.05 cardinal inputs (tests deadzone and near zero sensitivity)


----------

----------

### Electrical Specifications:

Manufacturer Recommended Source Voltage: 5V
Manufacturer Voltage Range: +/- 1.5V from Center
Manufacturer Center Voltage Drift: 0.3V

.

At 5V:
Center Voltage: 2.5V
Voltage Range: +/- 1V From Center 
    (1.53V - 3.44V Y)

![image](https://github.com/Sharp-02/Sanwa-JLM-UnOff-Documentation/assets/86936750/717e3b7c-39fd-46f3-a331-3865acd09732)

Current Draw at 5V: Estimated 50 mA

#### Hall Effect Board:

This board is encased in plastic below the JLM and provides the sensing of the lever angle through use of the on-board hall effect sensors.
<img src="https://github.com/Sharp-02/Sanwa-JLM-UnOff-Documentation/assets/86936750/86b95a9e-98a8-4e4e-9e8c-9e5223cbfe30" width=30% height=30%>
<img src="https://github.com/Sharp-02/Sanwa-JLM-UnOff-Documentation/assets/86936750/77d529e7-0619-4ad5-95e8-3a3489f6aa48" width=30% height=30%>

It is unclear whether or not the Sanwa JLM utilizes a 3D hall effect sensor and a microcontroller or a combination of a planar hall effect sensor and a switching hall effect sensor.

Evidence for the latter exists in the on-board IC connections. The connection of the U2 center pin is ambiguous, but one pin of the U2 IC is conneced directly to the switch pin. Pins 4 and 5 of U1 connect directly to the Y (green wire) and X (blue wire) axis output pins. This would also explain the correlation between voltage range and voltage supply, as well as the disconnect in the supply voltage required for the switching behavior compared to the analog axis behavior.

The specific IC components for both U1 and U2 are currently unknown. Likely, U1 is a planar hall effect sensor, while U2 is a switching hall effect sensor.

Clearer image of U2 IC part number:

<img src="https://github.com/Sharp-02/Sanwa-JLM-UnOff-Documentation/assets/86936750/99a4983f-6ac1-41b3-8b7e-2fd25335ff15" width=30% height=30%>
