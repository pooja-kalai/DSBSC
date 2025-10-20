# DSBSC USING PYTHON


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR USING PYTHON

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics.

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	CO LAB.

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f

Program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 3       
Ac = 6      
fm = 194    
fc = 1940    
fs = 19400   
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```

Output Graph:
![WhatsApp Image 2025-09-10 at 09 56 41_dfabd509](https://github.com/user-attachments/assets/6f32d458-1b0d-44dc-9832-1e2ad34e0ccf)

Tablular Column
![WhatsApp Image 2025-10-20 at 21 17 52_62e845aa](https://github.com/user-attachments/assets/a3f47004-e06c-43ec-8808-19a85662e66b)

Result:

Thus the DSB-SC-AM Modulation and Demodulation using python is generated.
