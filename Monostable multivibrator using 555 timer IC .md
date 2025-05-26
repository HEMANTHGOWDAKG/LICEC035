# Monostable multivibrator using 555 timer IC .
## Aim
### Generate pulse of width 0.5 ms using input triggers.
## Theory
A monostable multivibrator, often referred to as a one-shot circuit, has only one stable state. It’s built to generate a single output pulse—either high or low—for a set duration whenever it receives an external trigger.

When a trigger signal is applied, the circuit kicks off a timing process that temporarily shifts the output from its stable state. The time it stays in this unstable condition is determined by the RC time constant, which depends on the values of a resistor (R) and capacitor (C) in the feedback loop. After this preset time period, the output automatically returns to its original stable state and waits there until it gets triggered again.

These circuits are ideal for producing rectangular pulses that last longer. The start of the pulse happens exactly when the trigger signal is applied, while the end of the pulse is controlled by the RC time delay. By changing the R and C values, you can adjust the timing and generate a consistent series of delayed pulses based on each trigger.
## Working

In a 555 timer-based monostable multivibrator, the output remains in its low (stable) state until it receives a trigger signal. This stable state is maintained when the internal transistor is conducting and the capacitor is essentially discharged.

When the voltage at pin 2 of the 555 IC drops below a certain threshold (typically 1/3 of Vcc), the output instantly switches to a high state—this is known as the quasi-stable state. At this point, the internal discharge transistor turns off, and the capacitor starts charging toward the supply voltage (Vcc) through the resistor R1. The charging process is controlled by the RC time constant of R1 and C1.

As the capacitor voltage increases, it continues charging until it reaches 2/3 of Vcc. Once it crosses this point, the 555’s internal flip-flop is reset, causing the output to return to its original low (stable) state.

The duration of the output pulse (T) is given by the formula:
T = 1.1 × R × C
where R is the resistance in ohms , and C is the capacitance in farads (F).

In summary, a monostable multivibrator using a 555 timer stays low until triggered. After receiving a trigger pulse, the output goes high for a calculated duration (based on R and C), and then it automatically returns to low. This setup is commonly used in applications like push-button pulse generators, where a single press produces a well-timed output.
## Circuit Diagram:
![image](https://github.com/user-attachments/assets/bb37f20b-66b4-4744-901d-e0262de2926d)

## Calculation:
Given that T=0.5ms and assume c=.1uF.

T=1.1RC



R =  0.5mS/(1.1×1uF) = 4.5454 KΩ.
 
## Output Waveform
![image](https://github.com/user-attachments/assets/4ff3113f-d845-4684-b053-e50b7d29faac)

In the above circuit when the trigger pulse is lesser then 1/3 Vcc, We get output as high.

## Inference
1.In a monostable multivibrator circuit using a 555 timer, the default output state is LOW. This means that, under normal conditions, the output stays low until an external trigger is applied.

2.When a trigger signal is received (usually a momentary drop in voltage at pin 2), the output immediately switches from LOW to HIGH. This high output is not permanent—it lasts only for a specific period, which is precisely determined by the product of a resistor (R) and capacitor (C) connected in the timing network. This product is referred to as the RC time constant.

3.For example, let’s say we choose a capacitor with a value of 0.1 µF (microfarads). To produce a pulse width (or output duration) of 0.5 milliseconds, we can calculate the required resistor value using the standard monostable formula:
T = 1.1 × R × C
Plugging in the values:
0.5 ms = 1.1 × R × 0.1 µF
Solving this, we find R ≈ 4.5454 kΩ.
This shows how specific timing can be achieved just by selecting appropriate component values.

4.This experiment clearly demonstrates the functionality of the 555 timer in monostable mode. By using it in this configuration, we can create precise, one-shot output pulses that are extremely useful in applications requiring accurate timing or delay, such as debouncing buttons, triggering relays, or generating time-controlled signals in digital circuits.
# Astable multivibrator and monostable multivibrator using 555 timer IC
## Aim
## Generate pulse of width 0.5ms using 555 timer IC.
## Theory 
A monostable multivibrator (or one-shot) has only one stable state. When it receives a trigger pulse, it switches temporarily to an unstable state and produces a single output pulse of a set duration.

The time the output stays in the unstable state depends on an RC time constant, determined by a resistor (R) and a capacitor (C) in the circuit. After this time passes, the output returns to its original stable state and waits for the next trigger.

This circuit generates long rectangular pulses, where the rising edge of the pulse starts with the trigger, and the falling edge is delayed based on the RC values. By changing R or C, the pulse width and delay can be adjusted.

## Working
In a 555 timer-based monostable circuit, the output stays LOW by default. This state is maintained until the circuit gets a trigger signal.

When the voltage at pin 2 drops below 1/3 of Vcc, the output switches to HIGH—a temporary state called quasi-stable. The internal discharge transistor turns off, and the capacitor starts charging through resistor R1.

As the capacitor charges, its voltage increases. When it crosses 2/3 of Vcc, the 555 timer resets, and the output goes back to its stable LOW state.

The pulse width is given by the formula:
T = 1.1 × R × C
(where R is in ohms and C is in farads)

In short, the output stays LOW until triggered. Then it goes HIGH for a set time and returns to LOW. This is often used in push-button systems to generate a fixed-length pulse from a short input.




## Calculation
![image](https://github.com/user-attachments/assets/5c3bf55d-d0ef-4fa9-9bc1-6b2a09316c1f)


![image](https://github.com/user-attachments/assets/4166f3a0-c94a-4fe7-864e-e452be3a57fc)



## Circuit Diagram:
![image](https://github.com/user-attachments/assets/b07bcbbe-72dd-4548-a828-e1ff5dc9cebd)


## Waveform
### Case 1:
![image](https://github.com/user-attachments/assets/bdcbd7d8-b042-44d8-a02f-16989a367a90)

The first waveform is the continuous square wave output of the Astable Multivibrator. The second waveform shows the Differentiator Circuit output, which produces sharp spikes at the transitions of the square wave. The third waveform is from the Negative Clipper Circuit, which removes the negative parts of these spikes, passing only the positive portions. Finally, the fourth waveform is the output of the Monostable Multivibrator, generating a single pulse of 0.5 ms duration each time it is triggered by the clipper’s output.
### Case 2:
![image](https://github.com/user-attachments/assets/bb0dabe9-f63f-4be1-9e6b-fbbc78f23174)

The first waveform shows the output of the Astable Multivibrator. The second waveform is from the Differentiator Circuit, producing sharp spikes at the transitions of the square wave. The third waveform represents the output of the Negative Clipper Circuit, which removes the negative portions of these spikes. The fourth waveform is the output of the Monostable Multivibrator, generating a pulse with a width of 0.5 ms, using a capacitor value of 1uF.



 ### Case 3:

 in case 3 the ton<toff which is not possible in astable Multivibrator , thus we can use an inverter to invert the pulse generated.
 
![image](https://github.com/user-attachments/assets/62330045-4a0a-422d-b977-9699a629bb00)


 ![image](https://github.com/user-attachments/assets/5974cd20-b140-48e9-b307-9e661e8e4906)



First wave is output of inverted Astable Multivibrator, Second waveform is Output of Differentiator Circuit output, 3rd wave is the output of Negative Clipper circuit and fourth waveform is output of Monostable Multivibrator pulse width is 0.5ms.

## Inference
1.Controlling ON and OFF Times Can Be Tricky: While adjusting resistor and capacitor values allows us to control how long the output signal stays ON or OFF, it’s not always possible to achieve any desired timing with a basic 555 timer circuit.
2.Limitations of the 555 Timer: In some situations—such as when the OFF time must be longer than the ON time—the standard 555 astable circuit cannot directly produce the required waveform. For example, in Case 3, we had to use an inverter to flip the signal and get the desired timing.
3.Using Inverters for More Flexibility: Adding a simple NOT gate (built with a transistor) allowed us to invert the waveform, giving us greater control and flexibility in shaping the output signal.
4.Precise Components Are Needed for Very Short Pulses: In Case 2, where pulse durations were fractions of a millisecond, we used very small resistor and capacitor values. This highlighted how critical component accuracy is when working with fast timing.
5.Edge Detection with a Differentiator: A differentiator circuit helped us detect the precise moments when the signal transitions from LOW to HIGH. This is useful for triggering actions only on changes rather than during the entire pulse.
6.Monostable 555 Produces Clean Pulses: Triggering the monostable 555 with these detected edges resulted in clean, consistent output pulses. This ensures reliable timing regardless of how long the input signal lasts.


In Case 1, the circuit used a direct astable 555 timer output with ON time of 0.2 ms and OFF time of 0.3 ms. This setup demonstrated that basic control of ON and OFF durations using resistor (R1, R2) and capacitor (C) values works well within certain timing ranges.

For Case 2, the configuration involved generating high-speed pulses with very small resistor and capacitor values, producing an ON time of 0.1 ms and OFF time of 0.05 ms. This showed that fast switching is achievable but requires precise, low-value components, which are essential for generating very short pulses.

In Case 3, the ON time was 0.3 ms and OFF time was 0.4 ms, but this was achieved by adding an inverter stage after the 555 output. This case highlighted how using logical inversion can help overcome the 555 timer’s limitations, allowing for timing where the OFF period is longer than the ON period.



# Simulation in Virtual Lab Astable Multivibrator
## Procedure:
1.	Connect the components as mentioned below: L1-L12, L14-L12, L16-L12, L4-L9, L8-L9, L10-L19, L3-L17, L11-L13, L7-L19, L6-L13, L2-L13, L5-L15, L18-L9.(For eg. click on 1 and then drag to 12 and so on.)
2.	Click on 'Check Connection' button to check the connections.
3.	If connected wrong, click on the wrong connection. Else click on 'Delete all connection' button to erase all the connections.
4.	Intially set R a=3.3 kΩ, R b=6.8kΩ, C=0.1µf, Vcc=5 V.
5.	Click on "Calculate" button.
6.	Now note the output voltage.
7.	Click on "Plot" button to plot Output Voltage, Capacitance Voltage
8.	Click on "Clear" button to clear the data.
9.	Repeat the experiment for another set of resistance value.
10.	Set the Resistance (Ra) value (1 kΩ - 10 kΩ).
11.	Set the Resistance (Rb) value (1 kΩ - 10 kΩ).
12.	Set the Capacitance (C) value (0.1 µf - 10 µf) .
13.	Set supply voltage (Vcc).

## Circuit Diagram
![image](https://github.com/user-attachments/assets/303eba91-66eb-4a6a-9dbc-12f03dbb176c)


## Otuput Waveform
Voltage Across the Capacitor: 
![image](https://github.com/user-attachments/assets/3894310a-e307-4e17-a570-e0371812d10f)


Output Waveform: -
![image](https://github.com/user-attachments/assets/df261aa6-19a1-41bf-82f9-d65b0f5742c9)


 
