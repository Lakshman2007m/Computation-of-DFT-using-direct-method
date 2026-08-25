### EXPT 1: Computation-of-DFT-using-direct-method

### AIM
To perform and verify DFT using direct method by SCILAB.
### APPARATUS REQUIRED
PC installed with SCILAB
### PROGRAM 
### DFT DIRECT METHOD
```
clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
for k=0:N-1
for n=0:N-1
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle = atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum')
```
### CALCULATIONS:
<img width="902" height="902" alt="WhatsApp Image 2026-08-25 at 12 28 05" src="https://github.com/user-attachments/assets/499af7f7-b5e8-4a50-9551-0a58f28b45eb" />

### SAMPLE OUTPUT:
<img width="758" height="591" alt="Screenshot 2026-07-27 221018" src="https://github.com/user-attachments/assets/420eb246-eda9-40b8-87e5-95b6c3e93580" />




## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

