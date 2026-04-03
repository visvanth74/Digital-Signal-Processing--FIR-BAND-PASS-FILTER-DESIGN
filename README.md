# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen

clear all; % clear screen

close all; % close all figure windows

wc1=input('enter the value of cut off frequency wc1'); 

wc2=input('enter the value of cut off frequency wc2'); 

N=input('enter the value of filter'); 

alpha=(N-1)/2; 

eps=0.001; 

%Band Pass Filter Coefficient

n=0:1:N-1;

hd=(sin(wc1*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)

%Hanning Window Sequence  

n=0:1:N-1;  

wh=0.5-0.5*cos((2*pi*n)/(N-1)) 

hn=hd.*wh  

% Plot the Band Pass Filter with Hanning Window Technique

w=0:0.01:pi; 

h=freqz(hn,1,w);

plot(w/pi,abs(h),'blue');

## OUTPUT:
<img width="736" height="684" alt="image" src="https://github.com/user-attachments/assets/fe65774b-ac92-4d0e-bf10-2a713c15851f" />
## RESULT:
<img width="1280" height="375" alt="image" src="https://github.com/user-attachments/assets/0ef3bc8a-380e-4b60-bb2d-9bcef089d56c" />
