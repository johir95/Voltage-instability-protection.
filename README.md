# Voltage-instability-protection.
Objective:The main objective is to design a circuit that controls a load based on varying input voltages using a relay, transistors, and a 555 timer for delayed activation.The circuit responds differently to 180V (Low voltage the load will be OFF), 210V (Threshold voltage, the load will be ON after a 10-second delay), and 240V (High voltage, the load will be OFF).

Iist of Equipment: 
1. Transformer (220V-12V) 
2. Diode (1N4001) 
3. Capacitor  (  470u, 1000u ) 
4. Resistor   (1k, 15k,100k,10k)  
5. Zener Diode ( 1N4741A) 
6. Relay  (12V) 
7. LED   
8. Bulb (20W) 
9. IC-555      ( NE 555  ) 
10. Pot  (10k,100k)   
11. Transistor  (2N2222 ) 
12. Variac  
13. Project board   
14. House wiring cable   
15. Bulb holder


Working Principle 

Condition 1: 
When I supply 180V to the Primary side of the transformer then in the secondary side I 
have 9.8V after Rectifying. We use a Zener diode in the voltage of 12V.So if Q1 is active 
they need 12.7V to activated. So in the terminal R1 there was a voltage drop which is 
(1/1+10 * 9.8) and RV1 ther was also a voltage drop which is (10/1+10 * 9.8) .So in the 
zener dide terminal they have 9.7 V. So Q1 remain Off. Similarly Q2 will be off and 
when Q1 and Q2 will be off then relay will not energized and can’t move Normally Open 
(NO) terminal to the Normally Closed(NC) terminal. So the current can’t pass through a 
relay and the relay will be off also load will be OFF. 

 

Condition 2: 
When I supply 210V to the Primary side of the transformer then in the secondary side I 
have 11.54V after Rectifying. If Q1 is active they need 12.7V to activated (Zener diode 
voltage=12V and transistor volatge=0.7V). So in the terminal R1 there was a voltage 
drop which is (1/1+10 * 11.5) and RV1 ther was also a voltage drop which is (10/1+10 * 
11.5) .So in the zener dide terminal they have 11.54 V. So Q1 remain Off. Similarly Q2 
will be ON because in the transistor side the have 1.34V where it requires 0.7V to to ON 
condition, and when Q1 Off but Q2 will ON  so the emmiter and base terminal will be 
short and current flow through emitter to collector and for this relay will be energized and  
move Normally Open (NO) terminal to the Normally Closed(NC) terminal. So the 
current  pass through a relay and the relay will be ON  also load will be ON.But we set a 
condition in the 555 timer that when light will be ON it takes 10sec delay. So after 10sec 
Light will be ON.


Condition 3: 
The last case is When I supply 240V to the Primary side of the transformer then in the 
secondary side I have 13.2V after Rectifying. We use a Zener diode in the voltage of 
12V.So if Q1 is active they need 12.7V to activated. So in the terminal R1 there was a 
voltage drop which is (1/1+10 *13.2) and RV1 ther was also a voltage drop which is 
(10/1+10 * 13.2) .So in the zener dide terminal they have 12.77V. So Q1 will be ON. 
When Q1 will be ON then emmiter and collector will be short and the current pass to the 
ground through collector to emmiter terminal. So current can’t pass to the Q2 side and 
then relay won’t be energized so that load will be OFF 


10sec delay procedure: 
We connect a 470μF capacitor to the positive voltage supply and then to pin 2. We 
connect pin 6 to pin 2 and then connect a 22K resistor to ground. We connect pin 4, the 
reset pin, to the VCC. The reset pin is active low. So in order for reset not to be triggered, 
we connect this pin permanently HIGH. Pin 3 is the output pin. Therefore, we connect the 
LED along with the 470Ω resistor. 

 

The combination of the resistor and capacitor forms the RC network. This network 
determines the length of time it takes to charge the capacitor.The reason why the circuit 
doesn't turn on automatically is because pin 2, the trigger pin, initially when the power 
turns on, is HIGH. This is because the capacitor hasn't charged up yet. Until the capacitor 
charges up, this pin is HIGH. Since the trigger pin is active LOW, the output will be off 
until this pin goes LOW. As the capacitor charges up and gets near the supply voltage it 
is connected to, the voltage at pin 2 decreases. When the voltage at pin 2 gets below 1/3 
of the supply voltage, the pin is now LOW. When it is LOW, this is when the output goes 
HIGH and the LED turns on.There is a delay of about 10 seconds with this circuit. once 
you turn the power on, the LED doesn't turn on until about after 10 seconds.The RC 
network is what determines this. The bigger the resistor and capacitor value, the longer 
the delay. So if you want to increase the time of the delay, you would choose a bigger 
resistor and capacitor. If you want to shorten the time of the delay, you would choose a 
smaller resistor and capacitor value. And this is how a delay before turn on circuit works 
with a 555 timer




Application: 

Voltage instability has several real-world applications in the power system, including: 

Power System Planning and Design: Voltage stability analysis is used to evaluate the 
performance of power systems under different operating conditions and to identify 
potential voltage collapse scenarios. This information can be used to design power 
systems that are more resilient to voltage instability and to plan for mitigation measures. 

Power System Operation:Real-time monitoring and control systems are used to detect 
and prevent voltage instability during normal power system operation. This can include 
automatic voltage control systems, load shedding, and reactive power control. 

Renewable Energy Integration: With the increasing integration of renewable energy 
sources into the power system, voltage stability is becoming a more pressing issue. 
Analysis of voltage stability can help identify potential challenges posed by these new 
energy sources and guide efforts to integrate them into the power system in a stable and 
efficient manner. 

System Reliability: Voltage instability can lead to power outages and equipment 
damage, reducing the overall reliability of the power system. By detecting and preventing 
voltage instability, power system operators can improve the reliability of the system and 
reduce the risk of blackouts and Lightning Sparks. 
Overall, voltage stability is a critical aspect of power system operation, and its analysis 
and control play a vital role in ensuring the stability, reliability, and efficiency of the 
electrical power supply

















