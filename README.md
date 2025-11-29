# Mean-variance-cross-correlation

---

### Aim:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

---

### Equipments Required:

- Computer with i3 Processor 
- SCI LAB

---

### Algorithm:

1. Define the Function: Specify the function you want to simulate.
   For example,f(x)=sin⁡(x)f(x)=\sin(x)f(x)=sin(x) or any other function.
2. Generate Sample Points: Decide on the range and the number of sample points.
   Generate these sample points within the desired range.
3. Evaluate the Function: Compute the function values at each of these sample points.
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean
   and variance of the computed function values.
6. Display Results: Output the computed mean variance and Cross Correlation

---

### Procedure:

1. Refer algorithms and write code for the experiment.
2. Open Scilab in System
3. Type your code in the New Editor
4. Save the file
5. Execute the code
6. If any error, correct it in code and execute again.
7. Verify the generated results.

---

### Program:

```sci
clear;
clc;
clear;

function X = f(x)
    X = 2 * x .* (4 - x).^2;
end

a = 0;
b = 1;

EX = intg(a, b, f);

function Y = c(y)
    Y = 2 * y .* (4 - y).^2;
end

EY = intg(a, b, c);

mprintf("i)   Mean of X = %.2f\n     Mean of Y = %.2f\n", EX, EY);

function X = g(x)
    X = x.^2 .* 2 .* (4 - x).^2;
end

EX2 = intg(a, b, g);

function Y = h(y)
    Y = y.^2 .* 4 .* (3 + y).^2;
end

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

mprintf("ii)  Variance of X = %.6f\n     Variance of Y = %.6f\n", vX2, vY2);

x= input("type in the reference sequence="); 
y= input("type in the second sequence   =");

n1=max(size(y))-1;
n2=max(size(x))-1;

r=corr(x,y,n1);

clf();
plot2d3(1:length(r), r);
```

---

### Output Graph:
<img width="753" height="571" alt="image" src="https://github.com/user-attachments/assets/4c13793a-f52d-4c28-baa1-e595eb3921c8" />

---
### Output:

<img width="539" height="187" alt="Screenshot 2025-11-29 134355" src="https://github.com/user-attachments/assets/ea2f7f79-60ac-4f26-846d-0461428e7b40" />

---

### Tabulation:
![WhatsApp Image 2025-11-29 at 1 16 38 PM](https://github.com/user-attachments/assets/ffaaaf43-8e2e-4377-9414-94bb99bbfc3d)

---
### Calculation:

![WhatsApp Image 2025-11-29 at 1 28 43 PM](https://github.com/user-attachments/assets/bfc1a5dd-8ed1-4bfa-8260-49f7e20a19ae)

![WhatsApp Image 2025-11-29 at 1 29 02 PM](https://github.com/user-attachments/assets/047cf8c1-4032-45ec-b38d-1471b05c689a)



---

### Result:

Thus the mean, variance and cross correlation are executed in Scilab and the output is verified.
