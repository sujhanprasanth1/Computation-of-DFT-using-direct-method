# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
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

## CALCULATIONS:


<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/9482648c-a6a1-409b-a791-c2450d20d666" />
<img width="900" height="1600" alt="image" src="https://github.com/user-attachments/assets/69a25af3-86fd-441f-ab64-0ed67c07f524" />
<img width="319" height="529" alt="image" src="https://github.com/user-attachments/assets/f98dc0b6-f086-4957-bb78-d5ab099313af" />



### SAMPLE OUTPUT:
<img width="1600" height="745" alt="WhatsApp Image 2026-08-18 at 9 15 14 AM" src="https://github.com/user-attachments/assets/1b4f4097-7250-438a-bd6c-a4eb345cc4d7" />

<br>
<br>
<br>
<br>



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

