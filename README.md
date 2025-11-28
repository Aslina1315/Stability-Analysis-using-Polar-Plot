
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 22 39 55_6fd1d829](https://github.com/user-attachments/assets/72948cb9-4555-4e32-b5db-399138e4de97)
![WhatsApp Image 2025-11-27 at 22 40 15_dec7fa57](https://github.com/user-attachments/assets/805a07ea-306d-472a-986a-f971827f1a81)
![WhatsApp Image 2025-11-27 at 22 40 29_150bb49b](https://github.com/user-attachments/assets/839e18c4-8b7d-4a7e-bad0-0353c597d110)
<img width="896" height="1232" alt="image" src="https://github.com/user-attachments/assets/05e150b0-22e4-48ed-b128-570061dc8cda" />



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=[10]<br>
den=[0.1 0.7 1 0]<br>
sys=tf(num,den)<br>
[mag,phase,W]=bode(sys)<br>
mag=squeeze(mag)<br>
phase=squeeze(phase)<br>
phase1=deg2rad(phase)<br>
polarplot(phase1,mag,'linewidth',1.5)<br>
grid on<br>
[Gm Pm Wpc Wgc]=margin(sys)<br>
if(Wpc>Wgc)<br>
disp('stable')<br>
elseif(Wpc == Wgc)<br>
disp('marginally stable')<br>
else<br>
disp('unstable')<br>
end<br>

## Output:
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/03a27895-f728-4419-80b4-d292402bdab0" />


## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB<br>
Gain margin = 0.7<br>
Phase Margin = -8.88<br>
Gain crossover frequency = 3.75<br>
Phase crossover frequency = 3.16<br>
The system is unstable<br>
