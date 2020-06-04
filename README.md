# Water-level-controller-using-8051-Microcontroller
# Abstract
 <p> The main theme of our project is to save water, in addition to water level controlling in the tank, we will open the cap of the tank if we dectect the rain water and not only these, we have added another feature to our device by adding buzzer(alarm), so that it gives alarm when rain falls which help to bring back the items(clothes, eatables, etc.) that we have kept in sun light for drying.<br>
  <br>
  <b>Dividing project into parts for simplicity:</b><br>
  <br>
      1. Water level controller<br>
      2. Rain water detecction <br>
      3. Adding alaram       <br>
  <br>
<li><b>Water level controller</b></li><br>
  This project will help us in controlling the water motor by sensing the water level in a tank automatically. Here we should know how to detect and control the water level in an overhead tank or any container. This system monitors the water level of the tank and automatically switches ON the motor whenever tank is empty.
        
  The motor is switched OFF when the overhead tank or container is FULL. Here, the water level of the tank is indicated on LCD (Liquid crystal Display). Using this system, we can avoid the overflow of the water.Water is commonly used for agriculture, industry, and domestic consumption. Therefore, efficient use and water monitoring are potential constraint for home or office water management system. The existing automated method of level detection is described and that can be used to make a device on/off.

  Proper monitoring is needed to ensure water sustainability is actually being reached, with disbursement linked to sensing and automation. Such programmatic approach entails microcontroller based automated water level sensing and controlling.

  Water, one of the great natural resources should be utilized in proper form. But a huge amount of water is being wasted during daily life due to lack of control. Our proposed system guarantees to accumulate a good amount of usable water every day.<br>
<br>
<b>Hardware and software requirements:</b><br>

  <li>AT89C51 Microcontroller (or any 8051 based Microcontroller) [1].</li>  
  <li>8051 Programmer (Programming Board) </li> 
  <li>11.0592 MHz Quartz Crystal  </li>
  <li>2 x 33pF Capacitor</li>   
  <li>LCD </li>
  <li>2 x 10KΩ Resistor (1/4 Watt)  </li>
  <li>10µF Capacitor </li>  
  <li>Push Button   </li>
  <li>1KΩ x 8 Resistor Pack (for Pull – up)</li>
  <li>16 x 2 LCD Display</li>
  <li>5V Relay</li>
  <li>4 x 2N2222 (NPN) Transistors</li>
  <li>DC Motor (for demonstration)</li>
  <li>10KΩ Potentiometer</li>
  <li>1N4007 PN Junction Diode</li>
  <li>Programming cable</li>
  <li>Connecting wires</li>
  <li>Power Supply</li>
  <li>Buzzer</li>
  <li>Keil µVision IDE</li>
  <li>Willar Software (for burning code)</li>
  <li>Proteus (for circuit diagram)</li><br>
  <br>
<b>Water Level Controller using 8051 Circuit Principle</b><br>
This system mainly works on a principle that “water conducts electricity”. The four wires which are dipped into the tank will indicate the different water levels. Based on the outputs of these wires, microcontroller displays water level on LCD as well as controls the motor.

Initially when the tank is empty, LCD will display the message LOW and motor runs automatically. When water level reaches to half level, now LCD displays HALF and still motor runs.

When the tank is full, LCD displays FULL and motor automatically stops. Again, the motor runs when water level in the tank becomes LOW.<br>
<br>
<b>How to Design Circuit for Water Level Controller using 8051 Microcontroller?</b><br>
<br>
The heart of the Water Level Controller using 8051 Microcontroller project is the AT89C51 Microcontroller. The water level probes are connected to the P0.0, P0.1 and P0.2 through the transistors (they are connected to the base of the transistors through corresponding current limiting resistors). P0.0 for LOW level, P0.1 for HALF Level and P0.2 for HIGH Level.  

The Collector terminals of the Transistors are connected to VCC and the Emitter terminals are connected to PORT0 terminals (P0.0, P0.1 and P0.2). 

PORT1 of the microcontroller is connected to the data pins of LCD and the control pins RS, RW and EN of the LCD Display are connected to the P3.6, GND and P3.7 respectively.  

For demonstration purpose, we have used a simple DC Motor Pump. It is connected to the Relay and the input to the relay is fed from P0.7 through a transistor. <br> 
<br>
<b>Algorithm for Water Level Controller Circuit </b><br>
 <li>First configure the controller pins P0.0, P0.1 and P0.2 as inputs and P0.7 as output.</li>
 <li>Now, initialize the LCD.</li>
 <li>Continuously check the water level input pins P0.0, P0.1 and P0.2.</li>                                                            <li>If all the pins are low, then display tank as “EMPTY” on the LCD and make P0.7 pin HIGH to run the motor automatically.</li>
 <li>If the level is low i.e. if P0.0 is HIGH, display the water level as “LOW” and continue to run the motor. </li>
 <li>A HIGH pulse on the pin P0.1 indicates that water has reached half level. So, display the same thing on LCD and run the motor normally.</li>
 <li>If P0.2 is HIGH, then the water level in the tank is FULL.</li>
 <li>Now, make the P0.7 pin as LOW to turn off the motor automatically.</li><br>
<br>
<b>Circuit diagram:</b><br>


 <img src="Water level controller.jpeg">
 
 
 
  <b>Water Level Controller Circuit Advantages</b><br>
<li>Human effort is reduced as the system controls the motor automatically based on the water level.</li>
  
<li>This system consumes less power.</li>

<li>Simple and more reliable</li><br>

<b>Applications of Water Level Controller Circuit using 8051</b><br>
<li>Used in big buildings where the manual monitoring is difficult.</li>

<li>Used in industries to control the liquid level automatically.</li><br>

<b>How to Operate Water Level Controller Circuit using 8051 Microcontroller? </b><br>

1.	Initially, write the program for Water Level Controller in Keil µVision IDE and generate the .hex file.

2.	Burn the program (.hex file) to the microcontroller using external programmer and Willar Software.

3.	Now give the connections as per the circuit diagram.

4.	While giving the connections, make sure that there is no common connection between AC and DC supplies (if you are using an AC Motor)

5.	Place the 4 water level indicating wires into the small tank (3 probes for three different levels and fourth one for common supply)

6.	Switch on the supply. Now, the motor will run automatically as there is no water in the tank. (It will turn on even if the water level is LOW).

7.	Now pour the water, when it reaches LOW level, then LCD displays LOW.

8.	For middle level, it will display as HALF on the LCD.

9.	Still if you pour the water, then the water level reaches full and the LCD displays FULL and also the motor is turned OFF automatically.

10.	Switch off the motor supply and board supply.

<li><b>Circuit Simulation in Proteus software</b></li>

<img src="Water level controller simulation.png"><br>
<li><b>2. Collabing Rain water detection</b></li><br>
<b>Circuit diagram of Rain water detection</b>
<img src="Circuit-Diagram-8051-Microcontroller-Based-Rain-Detector.jpg">
<b> Improved simulation circuit</b> 
<img src="Water level controller with rain water detection.png">

We have to execute our program in a software(Keil) and then have to upload the generated .hex file into the microcontroller, after doing we have to run our simulation. By doing so, we will get the output as shown below.
<img src="Water level controller with rain water detection output1.png">
<img src="Water level controller with rain water detection output2.png">
</p>
