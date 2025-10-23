# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-1

__AIM:__

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation. 


__EQUIPMENTS Needed:__

.Computer with i3 Processor 

.SCI LAB


__THEORY:__

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the 
Fourier transform of the corresponding autocorrelation function.

__Algorithm:__

 1.Load or Define the Signal: Input your time-domain signal. 

 2.Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3.Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like
Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4.Plot Results: Visualize the autocorrelation function and PSD. 

__PROCEDURE:__


Refer Algorithms and write code for the experiment. 

Open SCILAB in System 

Type your code in New Editor 

Save the file 

Execute the code 

If any Error, correct it in code and execute again 

Verify the generated waveform using Tabulation and Model Waveform 

__PROGRAM:__

```
clc;
clear all;

T = 0:0.01:2*%pi;
x = sin(2*T);

subplot(3,2,1);
plot(x);

au = xcorr(x, x);
subplot(3,2,2);
plot(au);

v = fft(au);
subplot(3,2,3);
plot(abs(v));

fw = fft(x);
subplot(3,2,4);
plot(fw);

fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```

__OUTPUT:__

<img width="1859" height="883" alt="Screenshot 2025-10-16 161237" src="https://github.com/user-attachments/assets/f1979a0a-3649-4e6c-b139-ee13cb9d4375" />


__RESULT:__
Thus, a program for Autocorrelation and PSD of signals in SCILAB and verified Wiener-Khinchin relation. 
