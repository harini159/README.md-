
# AM using Python

EXP NO: 1 GENERATION AND DETECTION OF AM

AIM:

To generate and detect the amplitude modulation and demodulation u s i n g COLAB and to calculate modulation index of AM.

EQUIPMENTS REQUIRED

• Computer with i3 Processor

•Goolge COLAB

THEORY:

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing • Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

Under modulation : m<1, Em < Ec
Critical modulation: m-1, Em = Ec
Over modulation: m>1, Em > Ec
Note: Keep all the switch faults in off position.

Algorithm:
 
   1.Define Parameters set the following parameters:
   • Amplitude of message signal → Am
   • Frequency of message signal → fm
   • Sampling frequency → fs
   • Amplitude of carrier signal → Ac
   • Frequency of carrier signal → fc

   2.Create Time Vector
   Generate the time vector t for 2 cycles of the message signal:
     t = np.arange(0, 2/fm, 1/fs)

   3.Create Modulating Signal
   Define the message signal (modulating signal):
     m = Am * cos(2 * π * fm * t)
   
   4.Plot Modulating Signal
   Plot m in the first subplot using plt.subplot(3,1,1)
   
   5.Create Carrier Signal
   Define the carrier signal:
     c = Ac * cos(2 * π * fc * t)
   
   6.Plot Carrier Signal
   Plot c in the second subplot using plt.subplot(3,1,2)
   
   7.Perform Amplitude Modulation
   Generate the AM signal:
     Eam = (Ac + Am * cos(2 * π * fm * t)) * cos(2 * π * fc * t)
     
   8.Plot AM Signal
   Plot Eam in the third subplot using plt.subplot(3,1,3)
   
   9.Display All Plots
   Adjust layout with plt.tight_layout()
   Show the plots using plt.show()
   
   10.End of Program

Program:
  
   import numpy as np
   import matplotlib.pyplot as plt
   Am=2.18
   fm=274
   fs=27400
   Ac=3.14
   fc=2740
   t=np.arange(0,2/fm,1/fs)
   m=Am*np.cos(2*3.14*fm*t)
   plt.subplot(3,1,1)
   plt.plot(t,m)
   c=Ac*np.cos(2*3.14*fc*t)
   plt.subplot(3,1,2)
   plt.plot(t,c)
   Eam=(Ac+(Am*np.cos(2*3.14*fm*t)))*np.cos(2*3.14*fc*t)
   plt.subplot(3,1,3)
   plt.plot(t,Eam)
   plt.tight_layout()
   plt.show()

Output Waveform:


TABULATION:


Calculation:
   1.ma (Theory) = am/ac =
   2.ma(Practical) = (Emax-Emin)/(Emax+Emin) = 

MODEL GRAPH:

RESULT: Thus the amplitude modulation and demodulation is experimentally done and the output is verified.





