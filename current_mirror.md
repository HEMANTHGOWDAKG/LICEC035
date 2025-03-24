# Linear Integrated Circuit
# Current Mirroring Experiment
# PART-A
## Aim

Design and Analyze Current mirror circuit as active load in amplifier circuit.

**Given** :

Vdd=1.8V,P<=1mW,Av>-10V/V

## DC Analysis:(for mirror ratio 1:1)

WKT It=Iref+Ix<br>
So, for 1:1 ratio Iref=Ix<br>
i,e Iref=It/2<br>
It=1mW/1.8V<br>
It=0.555mA.<br>
Therefore,Iref=0.2778mA.<br>

To get the correct current based on the given ratio, the W/L values for M1, M2, and M3 are all set to 3um/180nm. The input voltage (Vin) is chosen to be 0.838V to ensure that the transistors are operating in the saturation region.

![Screenshot 2025-03-22 160459](https://github.com/user-attachments/assets/7b14e3ae-4e58-4e08-be20-b1616a220167)

**Obtained Output:**


![image](https://github.com/user-attachments/assets/4355a0b0-2ef2-40f0-a350-38a22bb70a93)


### Analyzing the current mirroring circuit by changing the w and L in same ratio.

**(a)L=180nm.**

WKT (w/L) ratio is 16.667.

Therefore for L=180nm the w=3um.

Mosfet M1: Id = 0.000277527

Mosfet M2: Id = 0.000277527

Mosfet M3: Id = 0.0002778           

**(b)L=500nm.**

WKT(w/L) ratio is 16.667.

Therefore for L=500nm the w=8.334um.

Mosfet M1: Id = 0.000281241

Mosfet M2: Id = 0.000281241

Mosfet M3: Id = 0.0002778          

**(c)L=1um.**

WKT (w/L) ratio is 16.667.

Therefore for L=1um the w=16.667um.


Mosfet M1: Id = 0.000280654

Mosfet M2: Id = 0.000280654

Mosfet M3: Id = 0.0002778            


## Transient Analysis:

#### Steps for transient Analysis:

* Replace DC input with an AC signal.
* Use SINE(dc_offset, Amplitude, Frequency).
* Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
* Set Stop Time: 10ms.
* Run the simulation.
* Our dc_offset = 0.838V and assume amplitude as 50mV and frequency as 1Khz.


![Screenshot 2025-03-22 160248](https://github.com/user-attachments/assets/44094458-400c-4e82-827a-17df48e34f91)



**OutPut Waveform:**
![image](https://github.com/user-attachments/assets/9e25f6c7-94e4-4da4-8726-217ab44f4c7b)


The expected gain of the circuit is -10V/V, but the actual gain from the transient analysis is -10.2V/V.There is only a small difference of 0.2V/V.


## AC Analysis:

![Screenshot 2025-03-22 155821](https://github.com/user-attachments/assets/cf266073-60a8-4493-8deb-4de5a19ba4c0)


#### Steps to get Ac analysis Waveform:
- In simulation tab select AC Analysis.
- In the AC Analysis tab, select **Type of Sweep as Decade**.
- Enter the number of points per decade (ex:20) and the frequency range ( 0.1Hz to 1THz).

**OutPut Waveform:**

![image](https://github.com/user-attachments/assets/b12cea30-c6c7-4774-b243-b67b23ebcb15)


The Expected gain in db of the circuit is 20db.But the obtained gain from the AC analysis(frequency response) is 22.16db.

Av (in dB):

Theory value = 20dB

Practical value = 22.16dB

Av (in V/V):

Theory value = 10

Practical value = 10.2


## DC Analysis:(for mirror ratio 1:2)

As we know It=Iref+Ix<br>
Therefore, for 1:2 ratio 2*Iref=Ix<br>
So,Iref=It/3<br>
It=P/Vdd<br>
It=1mW/1.8V<br>
It=0.555mA.<br>
Therefore,Iref=0.185mA.<br>

To obtain the current value according to the given ratio, the provided values of W/L for M1 is 6um/180nm , M2 is 6um/180nm, and M3 is 3um/180nm.<br>
Vin is selected in such a way that it should be in saturation region so the given Vin is 0.763V.<br>

![Screenshot 2025-03-22 162611](https://github.com/user-attachments/assets/6265822a-0538-4dcd-b93a-5d664c7ca5ff)


**Obtained Output:**

![image](https://github.com/user-attachments/assets/c40a002e-ec4d-47b9-b81a-04ae077c6152)



## Transient Analysis:

#### Steps for transient Analysis:

* Replace DC input with an AC signal.
* Use SINE(dc_offset, Amplitude, Frequency).
* Go to "Simulate" > "Edit Simulation Cmd" > "Transient".
* Set Stop Time: 10ms.
* Run the simulation.
* Our dc_offset = 0.763V and assume amplitude as 50mV and frequency as 1Khz.


![Screenshot 2025-03-22 162219](https://github.com/user-attachments/assets/3e54254a-e03f-4c8d-8a6d-e4550452668b)





**OutPut Waveform:**

![image](https://github.com/user-attachments/assets/e698ba15-55e3-4c19-a83e-e79578d46de4)



The Expected gain of the circuit is -10V/V.But the obtained gain from the transient analysis is -11.68V/V.


## AC Analysis:

![Screenshot 2025-03-22 162419](https://github.com/user-attachments/assets/34d2b2ce-9f72-4460-8a30-33eacf63de72)



#### Steps to get Ac analysis Waveform:
- In simulation tab select AC Analysis.
- In the AC Analysis tab, select **Type of Sweep as Decade**.
- Enter the number of points per decade (ex:20) and the frequency range ( 0.1Hz to 1THz).

**OutPut Waveform:**

![image](https://github.com/user-attachments/assets/e9acaf5f-fe52-4e3b-9768-f46b30462251)



The Expected gain in db of the circuit is 21.34db.But the obtained gain from the AC analysis(frequency response) is 24.6db.

Av (in dB):

Theory value = 21.34dB

Practical value = 24.6dB

Av (in V/V):

Theory value = 10

Practical value = 11.68


### Inference:
The current mirror circuit works well, accurately copying the reference current with very little variation, even when the W/L ratio changes. As the W/L ratio is adjusted, the drain current (Id) stays almost the same, showing that the circuit is effectively replicating the current.

Regarding the amplifier's performance, the gain is a little higher than what theory predicted in both mirror ratios. This small difference is likely due to slight mismatches in transistor parameters or simulation errors.

When the mirror ratio is increased from 1:1 to 1:2, the gain increases as expected. However, this also reduces the bandwidth, dropping it from 2.267 GHz to 1.173 GHz.

Overall, the results are very close to what theory predicts, confirming that the simulation and circuit are working as expected.

---------------------------------------------------------------------------------------------   


# PART-B
## Aim
Design the differential amplifier using the same design specification as Experiment-3.
Perform DC analysis,trasient and AC analysis.

### DC Analysis:

![a2](https://github.com/user-attachments/assets/7a288378-fe12-443a-a758-d9724e716933)

**Output:**

![image](https://github.com/user-attachments/assets/133ae875-a564-4643-8830-d737bea75bdd)

### Transient Analysis:

![a4](https://github.com/user-attachments/assets/5f5d6e0d-2fd0-4915-9d98-32dcdca55315)


**Output Waveform:**

![image](https://github.com/user-attachments/assets/2b93a042-6ea7-410c-b785-f82b95207c61)


### AC Analysis:


![a6](https://github.com/user-attachments/assets/7f25c62d-aef6-4887-ae26-ed3e339e19ff)



**Output Waveform:**


![image](https://github.com/user-attachments/assets/3b9e29f3-9baf-46d9-abe0-92999b9fb33b)

