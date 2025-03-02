# Expeiment-3

## Aim:
Design and Analyze the MOS differential amplifier circuit for the following specifcations and Perform DC analysis,Transient Analysis,Frequency response and extract parmeter

VDD=2v,P<=1mW,Vicm=1v,Vocm=1.1v,Vp=0.4v

#### Differential Amplifier:

differential amplifiers  consist of two transistors M1 and M2, whose sources are joined together. If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same.This configuration is called "Common Mode input voltage differential Amplifier".WHatever may be the load resistor, the MOSFET M1 and M2 should not go to the Triode region. It should be verified that MOSFET should be in Saturation Region.

For all this circuit we need find out the AC analysis ,Transient analysis And Frequency Response.
# Circuit-1
Components Required: MOSFET(M1,M2 and M3), Resistor,voltage supply's 
![ex3 cr1](https://github.com/user-attachments/assets/85772e76-3185-4a98-b7b7-a9bab4324d2d)



Procedure :
Make the circuit connection as given above.
connect the resister at the source terminal of both mosfet 
now calculate the value of Iss as power and vdd is given
and calculate the Id1 and Id2 
now calculate the Rss and Rd 

Now to get the desired values of output voltage and current we have to vary the width and length of both the mosfet
we got L=3um and W=210um 


![ex3 wl](https://github.com/user-attachments/assets/26f02ae4-6e27-4b53-b270-216cb2e45bc0)




# DC analysis:


   To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation
   the figure below is the values obtained from the DC analysis

![ex3 dc cr1](https://github.com/user-attachments/assets/757fb625-4426-4731-bced-723195189cc2)


Here in dc analysis we got the vout as expected and id1 and id2 we got the same 


# Transient analysis:

  To perform transient analysis we have to select the transient analysis in the edit simulation
   and give the stop time as 5ms and run the simulation .
   and the graph velow shows the transient response of the design.

   ![trs cr1](https://github.com/user-attachments/assets/05940269-53b6-4adf-a9bd-677e12c0d0db)


# AC analysis:

   TO perform AC analysis we have to select the ac analysis in the edit simulation command given the values as shown below

   ![Screenshot 2025-02-17 184334](https://github.com/user-attachments/assets/b5b9b5b2-cc27-459c-87d9-27411895f901)
 

   ![1 4](https://github.com/user-attachments/assets/e38ceac5-13a9-46b8-ad3c-efeac570178f)





# Circuit-2:


Now replace the R3 resister with a current source :
connect a current souce of 1mA

![CR2](https://github.com/user-attachments/assets/430f3b32-16ef-4a4f-9659-4d480f7fc0bd)




# DC analysis:

  To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation
   the figure below is the values obtained from the DC analysis

  ![image](https://github.com/user-attachments/assets/4bbeecff-a87f-46a7-abb8-e6647fc67049)



   # Trasient analysis:

  To perform transient analysis we have to select the transient analysis in the edit simulation
   and give the stop time as 5ms and run the simulation .
   and the graph velow shows the transient response of the design

   
   we have to give deg of 180deg to one mosfet and 0deg to the other mosfet
   and ac amplitude 1 for one mosfet and 0 for other mosfet
  ![Screenshot 2025-03-02 130322](https://github.com/user-attachments/assets/9ae919cf-f16c-4df7-ac50-e22cc623c2f2)




 # AC analysis:
 
  <img width="959" alt="image" src="https://github.com/user-attachments/assets/98ec35e3-cac9-41a6-b2cf-5384f4559b01" />




  # Circuit-3:

  Now replace the R3 resister with a Mosfet  :
    Given vp=0.4v and wkt vt=0.36v we got the gate voltage of the new mosfet as 0.76v 

  ![cr3](https://github.com/user-attachments/assets/204c985a-6d9e-4906-8513-3d685449909b)


 To get the output voltage and vp and current desired value we have to 
 vary the width and length of the new mosfet
![Screenshot 2025-03-02 190203](https://github.com/user-attachments/assets/39f0a14a-c7f1-45ce-b951-6841a94a4e38)


# DC analysis:


<img width="472" alt="image" src="https://github.com/user-attachments/assets/417842be-d7ad-4955-8086-b77ea97d490e" />

 # Transient analysis:
 give ac amplitude as 1 for one mosfet and 0 gor other mosfet 

 ![Screenshot 2025-03-02 123127](https://github.com/user-attachments/assets/431d7132-e2fb-4870-b625-a5334a2e9a9d)

# AC analysis:
<img width="959" alt="image" src="https://github.com/user-attachments/assets/56a10839-f8b8-40e4-8c2f-a01d9dda29f3" />


# Result
1.VDD = 2V for power supply.
2.Biasing: The gate-source voltage (V_GS) of each transistor is set to 0.4V, with the differential pair's tail current adjusted to ensure proper saturation.
3.Input Voltage: The differential input is represented as a small signal Vin , with a DC bias point of 1.1V for the operating voltage.

After performing DC, transient, and frequency response analyses in PSIM, the amplifier shows stable biasing and good amplification of the differential signal with a high voltage gain at low frequencies, while the gain decreases as frequency increases, which is typical for such amplifiers.
  
# Inference 
The amplifier effectively amplifies small differential signals with a stable DC operating point, but its high-frequency response starts to degrade due to the inherent capacitances of the transistors. The extracted small-signal parameters indicate a decent voltage gain and manageable input/output resistances, making it suitable for low-frequency applications with moderate bandwidth.




   



   

   

   

