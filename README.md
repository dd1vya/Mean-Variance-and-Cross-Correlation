# SIMULATION OF MEAN AND VARIANCE USING SCILAB

### AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

### EQUIPMENTS Needed
 Computer with i3 Processor
 SCI LAB

### Algorithm
1. Define the Function: Specify the function you want to simulate. For example,
f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2. Generate Sample Points: Decide on the range and the number of sample points. Generate
these sample points within the desired range.
3. Evaluate the Function: Compute the function values at each of these sample points.
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the
mean and variance of the computed function values.
5. Display Results: Output the computed mean variance and Cross Correlation
   
### PROCEDURE
 Refer Algorithms and write code for the experiment.
 Open SCILAB in System
 Type your code in New Editor
 Save the file
 Execute the code
 If anyError, correct it in code and execute again
 Verify the generated results

### PROGRAM
~~~
clear;
clc;
clear;
//Mean Value
function X=f(x),
z=3*(1-x)^2,//Marginal Probability Density Function
X=x*z
endfunction
a=0;
b=1;
EX=intg(a,b,f);//Mean value of X
function Y=c(y)
z=3*(1-y)^2,//Marginal Probability Density Function
Y=y*z
endfunction
EY=intg(a,b,c);//Mean value of Y
disp(EX,"i)Mean of X =")
disp(EY," Mean of Y =")
~~~

### Variance
~~~
function X=g(x),
z=3*(1-x)^2,//Marginal Probability Density Function
X=x^2*z
endfunction
a=0;
b=1;
EX2=intg(a,b,g);
function Y=h(y)
z=3*(1-y)^2,//Marginal Probability Density Function
Y=y^2*z
endfunction
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;//Variance of X
vY2=EY2-(EY)^2;//Variance of Y
disp(vX2,"ii)Variance of X");
disp(vY2," Variance of Y");
Cross Correlation
x= input("type in the reference sequence=");
y= input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
~~~

### OUTPUT
1)Mean of X = 0.25
Mean of Y = 0.25
2) Variance of X 0.0375
Variance of Y 0.0375
3)Cross Correlation
Type in the reference sequence = [1 2 3 4 5 6 7 8]
Type in the second sequence = [2 1 3 5 6 3 5 9]

### OUTPUT WAVEFORM
<img width="537" height="175" alt="image" src="https://github.com/user-attachments/assets/42019527-5399-4bbf-a058-cb8e8a8cf6f8" />
<img width="660" height="525" alt="image" src="https://github.com/user-attachments/assets/47b64e51-36f1-4596-a22e-a3aa329c73b5" />


### TABULAR COLUMN
![WhatsApp Image 2025-10-24 at 19 36 34_bf4ecf1f](https://github.com/user-attachments/assets/11b8c134-bda0-40c1-ac36-9bfbfa264290)
![WhatsApp Image 2025-10-24 at 19 36 34_e94e7750](https://github.com/user-attachments/assets/7c9c029e-1fa7-45b9-b1ff-21379b1f172e)


### RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified
