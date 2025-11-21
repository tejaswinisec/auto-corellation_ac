<h1>AUTO-CORRELATION-AND-PSD</h1>

<h2>Aim</h2>

Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

<h2>Equipments Needed</h2>

Computer with Intel i3 processor (or higher)
Scilab software

<h2>Theory</h2>

The Wiener–Khinchin theorem states that:

The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

<img width="1062" height="301" alt="image" src="https://github.com/user-attachments/assets/868c6220-9932-4b72-80db-63e44ba4c85e" />

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

<h2>Algorithm</h2>

Load or Define the Signal: Input your time-domain signal.
Compute Autocorrelation: Calculate the autocorrelation function of the signal.
Compute Power Spectral Density (PSD):
Estimate the PSD using either:
Fourier Transform of the autocorrelation function, or
Methods like Welch’s periodogram.
Plot Results: Visualize both the autocorrelation function and PSD.

<h2>Procedure</h2>

Refer to the algorithm and write the code for the experiment.
Open Scilab on your system.
Type your code in a new editor.
Save the file.
Execute the code.
If any errors occur, debug and re-run the program.
Verify the generated waveform using tabulation and model waveform comparison.

<h2>Program (Scilab Code)</h2>

```asm
t = 0:0.01:2*3.14;
x = 3.7*sin(4*t) + 4.5*cos(6*t);

subplot(3,2,1);
plot(x);

autcorr = xcorr(x, x);
subplot(3,2,2);
plot(autcorr);

psd = fft(autcorr);
subplot(3,2,3);
plot(psd);

fw = fft(x);
subplot(3,2,4);
plot(fw);

fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```  
<h2>Output</h2>

<img width="1918" height="1008" alt="image" src="https://github.com/user-attachments/assets/dd70a05f-e769-4fa2-b3af-989a40f4ea92" />

<h2>Result</h2>

Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
