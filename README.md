# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~
clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
wc=input('enter the value of cut off frequency');  
N=input('enter the value of filter');  
alpha=(N-1)/2;  
eps=0.001;  
%high Pass Filter Coefficient 
n=0:1:N-1;  
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps)) 
%Hanning Window Sequence  
n=0:1:N-1;  
wh=0.5-0.5*cos((2*pi*n)/(N-1))  
hn=hd.*wh  
% Plot the high Pass Filter with Hanning Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w);  
plot(w/pi,abs(h),'ms');
~~~
## OUTPUT:
<img width="700" height="628" alt="image" src="https://github.com/user-attachments/assets/a322c9ac-8d08-4b40-b846-851e0d3b40c0" />

## RESULT:
<img width="1600" height="596" alt="image" src="https://github.com/user-attachments/assets/b8c9debe-ef06-46e2-9498-54e53c8eadea" />

