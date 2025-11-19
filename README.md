# MEAN-AND-VARIANCE-USING-SCILAB

AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB


Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results


PROGRAM

```
clc;
clear;

function f = fx(x)
    z = 3*(1 - x)^2;
    f = x * z;
endfunction
a = 0; b = 1;
EX = intg(a, b, fx);

function g = gx(x)
    z = 3*(1 - x)^2;
    g = x^2 * z;
endfunction
EX2 = intg(a, b, gx);
vX2 = EX2 - (EX)^2;

function c = fy(y)
    z = 3*(1 - y)^2;
    c = y * z;
endfunction
EY = intg(a, b, fy);

function h = hy(y)
    z = 3*(1 - y)^2;
    h = y^2 * z;
endfunction
EY2 = intg(a, b, hy);
vY2 = EY2 - (EY)^2;

x = [1 2 3 4 5 6 7 8];
y = [2 1 3 5 6 3 5 9];
n1 = max(size(y)) - 1;
r = corr(x, y, n1);

disp("Mean of X = " + string(EX));
disp("Mean of Y = " + string(EY));
disp("Variance of X = " + string(vX2));
disp("Variance of Y = " + string(vY2));
disp("Cross Correlation = " + string(r));

scf(0);
plot2d3(r);
xtitle("Cross Correlation between x and y");
xlabel("Lags");
ylabel("Correlation");
```
OUTPUT
i)	Mean of X =	0.25 Mean of Y =	0.25

ii)	Variance of X	 0.0375 Variance of Y	0.0375

Cross Correlation
Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]
 
 
<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/d0d09999-9ffe-49eb-8d88-999c46689267" />

TABULAR COLUMN
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/f5a3d290-c433-4fc6-bc5b-a4b9d87b479e" />
<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/f0cd2605-dd34-4a4b-9472-3f410dbe235c" />









RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.



 
 









RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
