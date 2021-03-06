##General preparation parts

###Overview
This section is an overview of most parts for certain operations used in particular equipment in the laboratory. The goal of this list is to provide analysis to help planning and designing a universal platform, with micro-controller NodeMCU, to use in a wide variety of equipment, from measuring instruments to self-regulating tools.

###Table of contents

- [NodeMCU](#NodeMCU)
- [General equipment - basic parts](#General_parts)
 * [Display with rotary encoder](#Display)
 * [3 state switch](#Switch)
 * [Heat-bed](#Heat_bed)
- [Rotating equipment - basic parts](#Rotating_parts)
 * [Stepper motor](#Stepper)
 * [DC motor](#DC)
- [Measuring equipment - basic parts](#Measuring_parts)
 * [pH sensor](#PH)
 * [Temperature sensor](#temp)


###NodeMCU <a id="NodeMCU"></a>
![NodeMCU](http://www.seeedstudio.com/depot/images/113990105%201.jpg)
Source:http://www.seeedstudio.com/depot/images/113990105%201.jpg

The [NodeMCU](http://frightanic.com/iot/comparison-of-esp8266-nodemcu-development-boards/#v2) is an open-source development kit, it features 13 general purpose inputs/outputs (GPIO) each GPIO can be PWM and a built in ESP8266 Wi-fi module with a PCB antenna. It comes with a lua-based unformal firmware, or you can develop it in the arduino IDE environment. Due to its flexibleness, small size and low cost it fits in with the project requirements and goals.

###General equipment - basic parts <a id="General_parts"></a>

####Display with rotary encoder <a id="Display"></a>
For the best user interaction, a display with a rotary encoder will be implemented in all lab equipment. It will give a favorable overview of speed and duration for each process. The display menu will be arranged in rows, making it a simple and fast solution for scrolling througout all the settings.

####3 state switch <a id="Switch"></a>
Is used for switching between different modes of operation. Its uses differ from one application to another, from a manual full throttle, to an emergency stop. Its full functionality will be defined in the software.

####Heat-bed <a id="Heat_bed"></a>
A PCB Heat-bed, commonly used in 3D printing technology, is a great solution for the [Heating plate / slide warmer](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#heat-plate) or  [Magnetic stirrer](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#Magnetic-stirrer). Its slow heating process makes it appropriate for applications where lower(under 100°C) and more stable temperatures are preferred. Another advantage of the heat bed is its heat distribution as seen from the [Thermal picture](http://blog.brixandersen.dk/wp-content/uploads/IR003957.jpg). Together with a integrated thermistor it forms a self-regulating system, with the ability to heat up to a certain temperature and maintain it.


###Rotating equipment - basic parts <a id="Rotating_parts"></a>
![Rotating equipment](https://cloud.githubusercontent.com/assets/17159617/14168954/5cd9aafc-f725-11e5-80ed-7af6616375b1.jpg)
Source:http://bmskgroup.com/product/mixers-rotators-tubes/

The following list contains all basic parts used by rotating instruments for their operation. The list does not cover design features, which are specific for different types of equipment. In principle, all rotating lab equipment works the same way and differ mainly in the rotation speed and axis. 

####Stepper motor <a id="Stepper"></a>
Will be used in low RPM (15-100 rpm) devices such as the [rotating wheel](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#rotation-wheel) and [laboratory shaker](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#shaker), in cases where slow and controlled revolutions are favoured.

####DC motor <a id="DC"></a>
In certain cases, e.g. [vortex mixer](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#Vortex-mixer) or [centrifuge](https://github.com/symbiolab/bio-labware/blob/master/010_general_preparation.md#Centrifuge), speed around 15,000 rpm is necessary to generate enough force.  DC motors are a good solution for high speeds and low cost.


###Measuring equipment - basic parts <a id="Measuring_parts"></a>
![Measurnig_equipment](http://www.phidgets.com/wiki/images/6/6b/3550_0.jpg)

Source:http://www.phidgets.com/wiki/images/6/6b/3550_0.jpg

All in all, measurements in the laboratory are taken with a large variety of sensors. The most GPIO pin efficient way to go would be, to make a universal input for all types of sensors, but this delivers the dilemma of constant sensor calibration.

####pH sensor <a id="PH"></a>
Determining whether a sample is acid, neutral or basic is one of the fundamental bio-chemic tests, to know this we need to measure its pH value, which is deterined by the amount hydrogen ion (H+) concentration in the sample. The goal is to use a pH sensor to measure the pH value with 0,01 accuracy.

####Temperature sensor <a id="temp"></a>
Its main function is to measure the temperature, but with this data a lot of other equipment can adjust their operation accordingly. It will enable self-regulating processes which are crucial for long term consistency and reproducibility of experiments.
