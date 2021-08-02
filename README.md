# Phase-Locked-Loop(Google-Skywater 130nm Technology node)
Contents:
1. Introduction
2. Specifications
3. Schematics simulations
4. Layout simulations
5. Post Layout simulations


1.Introduction:

Phase Locked Loop(PLL): A phase-locked loop or phase lock loop (PLL) is a control system that generates an output signal whose phase is related to the phase of an input signal. There are several different types; the simplest is an electronic circuit consisting of a variable frequency oscillator and a phase detector in a feedback loop. The oscillator generates a periodic signal, and the phase detector compares the phase of that signal with the phase of the input periodic signal, adjusting the oscillator to keep the phases matched.

Keeping the input and output phase in lock step also implies keeping the input and output frequencies the same. Consequently, in addition to synchronizing signals, a phase-locked loop can track an input frequency, or it can generate a frequency that is a multiple of the input frequency. These properties are used for computer clock synchronization, demodulation, and frequency synthesis.

![PLL loop](https://user-images.githubusercontent.com/83840023/127780271-9c39ef8a-250a-4bdb-aa5a-abd9b37b78a7.png)

(i) Phase Frequency detector: As the name implies, this circuit block within the PLL compares the phase of two signals and generates a voltage according to the phase difference between the two signals.

![PFD](https://user-images.githubusercontent.com/83840023/127793453-5defb3ae-fcaa-44c6-a458-ad68449b242f.JPG)

(ii) Charge Pump:
PFD generates the digital signal, but the input to the VCO is an analogue signal, thus Charge Pump converts the output of the PFD into analogue signal. This can be done through "Current Steering" circuit ie. by charging and discharging of the capacitor. But why only the capacitor is used and not a resistive load, this is because we are interested in the avarage time of [UP-DOWN] which is achieved by observing the voltage of capacitor.

![CP](https://user-images.githubusercontent.com/83840023/127793803-a29faf96-d242-4504-ac4b-5613501a4965.JPG)

(iii) Loop Filter:
This filter is used to filter the output from the phase comparator in the phase locked loop, PLL. It is used to remove any components of the signals of which the phase is being compared from the VCO line, i.e. the reference and VCO input. It also governs many of the characteristics of the loop including the loop stability, speed of lock, etc.

(iv) Voltage Controlled Oscillator:
The voltage controlled oscillator is the circuit block that generates the radio frequency signal that is normally considered as the output of the loop. Its frequency can be controlled over the operational frequency band required for the loop.

![VCO](https://user-images.githubusercontent.com/83840023/127793915-c5a2265c-8d8c-4612-8a46-1cab2303cd3c.JPG)

(v) Frequency Divider:

The VCO output is modulated to different frequencies using the frequency divider. 

![FD](https://user-images.githubusercontent.com/83840023/127794320-53227dae-a2a3-4396-9aae-4915bbd7b2bb.JPG)

2. Specifications
  
 1. Corner - TT(typical-typical) 
 2. Supply Voltage - 1.8Volts
 3. Room Temperature
 4. Input frequency fmin = 5MHz fmax = 12.5 MHz
 5. N = 8 (Multiplier)
 6. Jitter(RMS) <~ 20nsec
 7. Duty Cycle = 50%


3. PLL Pre-Layout Schematic Simulation:

![PLL_Prelayout_simulation](https://user-images.githubusercontent.com/83840023/127794612-31896a38-f860-47bf-b5d9-46e839e0aaeb.JPG)

4. PLL Layout:

![PLL Layout](https://user-images.githubusercontent.com/83840023/127794797-be5c7bac-6f25-4c9e-b1e2-b8aa52740a28.JPG)

5. Post Layout Simulation

![PLL_Postlayout_simulation](https://user-images.githubusercontent.com/83840023/127794891-275a26ed-7863-4f5a-821d-b1b863728ecd.jpg)











  
  



