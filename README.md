# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
Wc1=input('enter the value of Wc1=');  
Wc2=input('enter the value of Wc2=');  
N=input('enter the value of N='); 
alpha=(N-1)/2;  
eps=0.001;  
%Band Stop Filter Coefficient 
n=0:1:N-1;  
hd=(sin(Wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./(pi*(n-alpha+eps)) 
%Bartlett Window Sequence  
n=0:1:N-1;  
wh= 1-2*abs(n-alpha)/N
hn=hd.*wh 
% Plot the Band Stop Filter with Bartlett
% Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'ms');
```
## OUTPUT:
<img width="693" height="616" alt="Screenshot 2026-03-26 104608" src="https://github.com/user-attachments/assets/f4fcdb7c-6a1b-40e6-aa80-3fe29d7a861a" />

## RESULT:
![WhatsApp Image 2026-04-03 at 12 19 50 PM (1)](https://github.com/user-attachments/assets/c47f8e8b-63e8-4867-a7c9-1a8c590b65a5)
