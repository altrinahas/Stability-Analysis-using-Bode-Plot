# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 21 52 51_9529a906](https://github.com/user-attachments/assets/e77e832f-ebf9-49b0-8e74-e237a1f216f0)
![WhatsApp Image 2025-11-27 at 21 52 52_a418486f](https://github.com/user-attachments/assets/c2bbfb4f-047f-4fa1-8300-86b9cf8225a9)
![WhatsApp Image 2025-11-27 at 21 52 53_81c86a62](https://github.com/user-attachments/assets/5235f45e-6122-44b8-b6e8-812cd539cbf8)
![WhatsApp Image 2025-11-27 at 21 53 03_0059e88a](https://github.com/user-attachments/assets/3aedc970-2467-4f67-a6f9-a2a495c7a802)
![WhatsApp Image 2025-11-27 at 21 53 04_4ff34928](https://github.com/user-attachments/assets/b3335ee1-1dfd-4947-9c25-bea337bd87a9)



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:
<img width="702" height="629" alt="image" src="https://github.com/user-attachments/assets/ca0bd8f1-af72-4feb-b865-41174fbd80cf" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60.42 <br>
Gain crossover frequency =  0.90 <br>
Phase crossover frequency = 4.47 <br>
The system is stable
