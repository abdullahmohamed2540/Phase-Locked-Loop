# Phase-Locked-Loop
Design PLL in 130nm 
![127750108-df95ef4c-b283-4c7a-b14e-1d5fd7333671](https://user-images.githubusercontent.com/65411629/127780909-65694659-8320-45c2-80d2-4019e8a330df.png)
It is the  Workshop to Become a fullest in PLL using skywater-pdk using Google SkyWater 130nm Technology.The spice simulations were done using the Ngspice Open source EDA.
The Layout design using Magic and parasitic extraction.
The Workshop Carried Out in the below manner:
<br>
<h2>Day-1 : Basics of PLL </h2>

# Table of Contents

1. [About PLL and its application](#about)

2. [Componets of PLL](#Componets)

3. [Important terms in PLL](#terms)

4. [Design Flow and Lab setup](#design)

5. [Specifiation](#sepcs)

6. [Day 2- Pre and Post simulation](#pre) 

<hr>

## 1.About PLL and its application <a name="about"></a>
  
  <h4>A phase-locked loop or phase lock loop (PLL), it is an control system that generates  output signal whose phase is mimic to the phase of an input signal.it is an important Basic block for radio Frequency application.</h4>
<h3>Block Diagram</h3>

![p (2)](https://user-images.githubusercontent.com/65411629/127902294-4fc958aa-c9b6-4579-90a3-c3ac504d13da.png)

<p>It has two parts compare frequency and frequency mather, Compare frequency helps to compare the difference between the reference and feedback frequency. Frequency mather helps to adjust to mimic feedback frequency with respect to input frequency.</p>
<h4> Application node:<h4>
  
![Phase-locked-loop-control-system](https://user-images.githubusercontent.com/65411629/127784223-5e9945ee-2686-40e2-b31a-76bc97653810.png)
<h5>It helps to control speed of a motor</h5>
<h4>More Application:</h4>
<ul>1.Used in demodulation of frequency modulation (FM)</ul>
<ul>2.Used in demodulation of frequency-shift keying (FSK)</ul>
<ul>3.generate Clock multipliers in microprocessors </ul>
  
<h3> 2.Componets of PLL <a name="Componets"></a></h3>

  <h3>1. Phase Frequency Detector</h3>
It helps to compare the reference frequency signal(RefCLK) with Output frequency signal(FBCLK) to find out the differnce in the signal. such that if a signal is leading then it termed as output as up. When the signal is down it says that output signal is lagging.

![pfdbl](https://user-images.githubusercontent.com/65411629/127902079-54c57396-9cd9-4cba-89ab-f14b83b63b1f.jpg)

 

![pfd](https://user-images.githubusercontent.com/65411629/127818205-9ce876ff-210b-49a0-9d95-11a555f6af6f.jpg)
   
<h3>2.Charge Pumb</h3>
  the output from phase frequency detector is given as input of charge pump.It converts digital measure of phase/frequeny difference into an analog control signal to control the oscillator.wave form of charge pump is shown

  ![pfd](https://user-images.githubusercontent.com/65411629/127901526-8f7926c7-fc66-4ae0-8813-dd3c855d8468.jpg)



<h3>3.Low Pass Filter</h3>
  It is the omplement of high pass filter.it passes signals with a frequency lower than a selected cutoff frequency and attenuates. WithouT THIS PLL doesm't Lock. 
  
  ![lp](https://user-images.githubusercontent.com/65411629/127825078-d8ce7f39-746b-497c-83d2-2ba58a811a16.jpg)
<h3> 4. Votage Controlled Oscillator</h3>
   It is an oscillator whose oscillation frequency is controlled by a voltage input.
  
  ![Phase-Frequency-Detector-Block-Diagram (2)](https://user-images.githubusercontent.com/65411629/127826611-895a5763-589a-4a92-8910-683a239912c7.png)

<h3>5. Frequency Divider</h3>
  It is a Concept of series of odd number of inverters,period = 2*delay(inverter)*inverter-count.
 
  ![fd](https://user-images.githubusercontent.com/65411629/127902550-28c66e83-1ac5-4388-aad9-779c350f1376.jpg)

 <h3>Important Terms In PLL <a name="terms"></a></h3>
  
  <h4>1. Lock Range</h4>
  PLL ia able to follow input frequency variation once it locked its destinct range.
  
  <h4>2.Capture Range</h4>
  The frequency range PLL is able to lock when starting from an unlocked condition.
  
  <h4>3.Setting Time</h4>
  The time within when the PLL is able to lock in form an unlocked condition.
  
  <h3>4. Design flow and Labsetup <a name="design"></a></h3>
  <h4>NgSpice Tool</h4>
  Intial flow start with targeted design in NgSpice.NgSpice directly simulates the circuit(.cir) file given and plots the results according to the specifications mentioned in the circuit file. To execute the circuite file, on the CMD window type :
directory_name_where_files_are_present file_name.cir
<h4>Magic Tool</h4>
  After down with NgSpice layout design will take place in magic. Magic is used for designing the layout file, writing the GDS file for fabrication and also to extracrt the parisitics. To execute the file, on the CMD window type :
directory magic -T technology_file_name_from_PDK layout_file
In this project, we have used sky130A.tech for the 130nm node technology from Google Skywater library.
<h3>5. Specification <a name="sepcs" ></a></h3>
 
 Corner = TT

Supply voltage = 1.8V

Temperature = Room temperature

Input Fmin= 5MHz , Fmax= 12.5MHz

Multiplier = 8x

Jitter (RMS) < 20ns

Duty cycle = 50%

<br>
 <hr>
<h2>Day 2 : PLL simulation (Prelayout and Postlayout) <a name="pre"></a></h2>
# Table of Contents

1. [PreLayout simulation](#prelayout)

2. [PostLayout simulation](#postlayout)

3. [Tabeout](#tape)

4. [Acknowlegement](#ackno)

  <hr>
<h3>1. PreLayout Simulation <a name="prelayout"></a></h3>
  It is the simulation before design the layout to verify the designed circuit giving the right output
  <h4>1.Phase Frequency Detector Simulation using ngspice</h4>
  
![pfdc](https://user-images.githubusercontent.com/65411629/127900130-58e12168-510f-4232-a4d1-120b42536dc8.jpg)

  <h4>2.Charge Pump simulation using ngspice</h4>
  
  ![cp](https://user-images.githubusercontent.com/65411629/127845363-227437ef-e0e7-4c39-9403-b7560ecd7a78.jpg)
  
  <h4>3.Voltage Controlled Oscillator</h4>
  
  ![vco](https://user-images.githubusercontent.com/65411629/127845508-8012c9f3-7d9e-4b3b-b163-9cc1aa302c5f.jpg)

  <h4>4.Frequeny Divider</h4>
  
  ![p-pdf](https://user-images.githubusercontent.com/65411629/127845601-b7df7fe6-8e27-4092-a5a6-25c731d9ade3.jpg)
  
  <h4>5.Phase Locked Loop</h4>
  
![pll40mhz](https://user-images.githubusercontent.com/65411629/127899313-b75412aa-0523-4a8f-8097-dc1ba8711e49.jpg)
  
  <h3>Post layout and Parasitic Extraction <a name="postlayout"></a></h3>
  <h4>1.Phase frequency Detector</h4>
  
  ![fpd](https://user-images.githubusercontent.com/65411629/127896763-e9df250c-bf8d-442d-bb99-c63cbc8fe0b6.PNG)
<h4>2.Charge Pump</h4>

  ![cd2](https://user-images.githubusercontent.com/65411629/127897120-1e3d94b7-4e06-43b0-9777-b884430850c3.PNG)
<h4>3.MUX</h4>

  ![mux - Copy](https://user-images.githubusercontent.com/65411629/127898062-fb3aaec4-0899-4f4a-aabb-5cc20fe6273f.PNG)

  <h4>4.Voltage Controlled Oscillator</h4>
  
  ![VCO_Layout](https://user-images.githubusercontent.com/65411629/127897933-53973352-992d-4162-ac63-e443e855c39b.jpg)
<h4>5. Frequency Divider</h4>
  
  ![fpd](https://user-images.githubusercontent.com/65411629/127898288-501d02ef-2f75-4790-8eec-f19004168296.PNG)

  <h3>Acknowlegement <a name="ackno"></a></h3>
  
1. I would like to thank Mr. Kunal Ghosh, co-founder VSD, for providing me with this wonderful 2-day workshop.

2. I would like to thank Ms. Lakshmi S, for fullest guiding on design of PLL.
