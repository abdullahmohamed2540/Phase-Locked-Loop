# Phase-Locked-Loop
Design PLL in 130nm 
![127750108-df95ef4c-b283-4c7a-b14e-1d5fd7333671](https://user-images.githubusercontent.com/65411629/127780909-65694659-8320-45c2-80d2-4019e8a330df.png)
It is the  Workshop to Become a fullest in PLL using skywater-pdk using Google SkyWater 130nm Technology.The spice simulations were done using the Ngspice Open source EDA.
The Layout design using Magic and parasitic extraction.
The Workshop Carried Out in the below manner:
<br>
<h2>Day-1 : Basics of PLL </h2>
<h2> Contents: </h2>
<ol>1. About PLL and its application</ol>
<ol>2. Componets of PLL</ol>
<ol>3. Important terms in PLL</ol>
<ol>4. Design Flow and Lab setup</ol>
<ol>5. Specifiation</ol>
<hr>
<h2>1. About PLL and its application</h2>
  
  <h4>A phase-locked loop or phase lock loop (PLL), it is an control system that generates  output signal whose phase is mimic to the phase of an input signal.it is an important Basic block for radio Frequency application.</h4>
<h3>Block Diagram</h3>
  
![p (2)](https://user-images.githubusercontent.com/65411629/127783600-f99d83ad-bd6c-495e-adda-205a8591692d.png)
<p>It has two parts compare frequency and frequency mather, Compare frequency helps to compare the difference between the reference and feedback frequency. Frequency mather helps to adjust to mimic feedback frequency with respect to input frequency.</p>
<h4> Application node:<h4>
  
![Phase-locked-loop-control-system](https://user-images.githubusercontent.com/65411629/127784223-5e9945ee-2686-40e2-b31a-76bc97653810.png)
<h5>It helps to control speed of a motor</h5>
<h4>More Application:</h4>
<ul>1.Used in demodulation of frequency modulation (FM)</ul>
<ul>2.Used in demodulation of frequency-shift keying (FSK)</ul>
<ul>3.generate Clock multipliers in microprocessors </ul>
  
  
<h2>2. Componets of PLL</h2>
  <h3>1. Phase Frequency Detector</h3>
It helps to compare the reference frequency signal(RefCLK) with Output frequency signal(FBCLK) to find out the differnce in the signal. such that if a signal is leading then it termed as output as up. When the signal is down it says that output signal is lagging.
![Phase-Frequency-Detector-Block-Diagram (2)](https://user-images.githubusercontent.com/65411629/127784340-5415b5e9-9e25-4163-a5a9-233ad9873d9f.png)
 Wave form and state diagram representation is attached below.
 
![pfd](https://user-images.githubusercontent.com/65411629/127818205-9ce876ff-210b-49a0-9d95-11a555f6af6f.jpg)
   
<h3>2.Charge Pumb</h3>
  the output from phase frequency detector is given as input of charge pump.It converts digital measure of phase/frequeny difference into an analog control signal to control the oscillator.

<br>
<h2>Day 2 : PLL simulation (Prelayout and Postlayout)</h2>
<h2> Contents:</h2>
<ol>1. PreLayout simulation</ol>
<ol>2. PostLayout simulation</ol>
<ol>3. Tabeout</ol>
<ol>4. Acknowlegement</ol>




