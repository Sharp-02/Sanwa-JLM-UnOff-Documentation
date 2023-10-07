# Sanwa JLM Unofficial Documentation
Non-affiliated documentation, deconstruction, and partial reverse engineering of the Sanwa JLM (Joystick Lever Magnetic).

----------

## Documentation Objectives:

### Physical Documentation
* Pictures and dimensions of joystick components
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

# Electrical Specifications:

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
