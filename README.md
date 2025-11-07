# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import  numpy as np
import matplotlib.pyplot as plt
Am=6.1
fm=483
Ac=12.2
fc=4830
fs=48300
b=6.2
t=np.arange(0, 2/fm, 1/fs)
m = Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c= Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=Ac*np.cos(2*3.14*fc*t+b*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)

plt.tight_layout()
```
Output Waveform

<img width="803" height="595" alt="Screenshot 2025-11-07 212310" src="https://github.com/user-attachments/assets/691bee8b-d0e8-4d5f-8bb7-7a4e5f183499" />

Tabular Column

<img width="1142" height="716" alt="Screenshot 2025-11-04 230915" src="https://github.com/user-attachments/assets/4732f66f-5828-45fc-8373-a99af1cd7bd5" />

Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
