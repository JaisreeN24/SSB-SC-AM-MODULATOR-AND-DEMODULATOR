# SSBSC-Modulation

# EXP NO: 3	SSB-SC-AM MODULATOR AND DEMODULATOR

## AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## PROCEDURE

· Refer Algorithms and write code for the experiment.

· Open SCILAB in System

· Type your code in New Editor

· Save the file

· Execute the code

· If any Error, correct it in code and execute again

· Verify the generated waveform using Tabulation and Model Wavefor



### Note: Keep all the switch faults in off position

## Algorithm:
1. Define Parameters:

· Fs: Sampling frequency.

· T: Duration of the signal.

· Fc: Carrier frequency.

· Fm: Frequency of the message signal.

· Amplitude: Maximum amplitude of the message signal.

2. Generate Signals:

· Message Signal: The baseband signal that will be modulated.

· Carrier Signal: A high-frequency signal used for modulation.

· Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.

3. SSBSC Modulation:

· Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.

4. SSBSC Demodulation:

· Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.

· Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.

5. Visualization:

Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.

## Program
```
Am=12.1;
fm=1482;
Ac=1.5*Am;
fc=10*fm;
fs=10*fc;
t=0:1/fs:2/fm;
em1=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em1)
ec1=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec1)
em2=Am*sin(2*3.14*fm*t);
ec2=Ac*sin(2*3.14*fc*t);
eDSBSC1=(em1.*ec1);
eDSBSC2=(em2.*ec2);
eLSB=eDSBSC1+eDSBSC2
subplot(4,1,3);
plot(t,eLSB)
eUSB=eDSBSC1-eDSBSC2
subplot(4,1,4);
plot(t,eUSB)



```


## Output Waveform
<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/f67e5422-dc21-41a3-ac2d-461a85d1e268" />


## TABULATION:
<img width="767" height="1362" alt="WhatsApp Image 2026-06-03 at 23 45 18" src="https://github.com/user-attachments/assets/06c84538-bc43-44ab-9e8d-06966a5d3944" />

## MODEL GRAPH
<img width="1615" height="767" alt="image" src="https://github.com/user-attachments/assets/10ce7063-77d8-4abf-bb44-3fb42a5cb9f6" />



## RESULT:
Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.
