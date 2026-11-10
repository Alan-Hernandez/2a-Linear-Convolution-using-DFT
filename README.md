# EXPT 2a: LINEAR CONVOLUTION-USING-DFT
# AIM

To perform and verify linear convolution operation of two given sequences using SCILAB.

# APPARATUS REQUIRED 

PC installed with SCILAB

# PROGRAM:

# LINEAR CONVOLUTION

clc;

clear;

x = [1 2 3 4];

h = [2 4 8 6];

m = length(x);

n = length(h);

a=0:1:m-1;

b=0:1:n-1;

subplot(3,1,1);

plot2d3(a,x);

xlabel('Time');

ylabel('Amplitude');

title('Graphical Representation of Input Signal X');

subplot(3,1,2);

plot2d3(b,h);

xlabel('Time');

ylabel('Amplitude');

title('Graphical Representation of Impulse Signal h');

for i = 1: n+m-1

conv_sum = 0;

for j = 1:i

if (((i-j+1) <= n)&(j <=m))

conv_sum = conv_sum + x(j)*h(i-j+1);

end;

y(i) = conv_sum;

end;

end;

disp(y,'Convolution Sum using Direct Formula Method = ')

subplot(3,1,3);

plot2d3(y)

title('Graphical Representation of output Signal y');

### CALCULATIONS:

<img width="704" height="1280" alt="image" src="https://github.com/user-attachments/assets/fe9d2cba-1aff-484a-a238-00c3c4ce12e7" />

<img width="792" height="1280" alt="image" src="https://github.com/user-attachments/assets/0a42a716-472a-4cbb-956d-b17e1d441235" />

<img width="648" height="1280" alt="image" src="https://github.com/user-attachments/assets/45d97bca-eaec-440d-acd8-5d09aa9e44d8" />

<img width="894" height="1280" alt="image" src="https://github.com/user-attachments/assets/ff238f0f-a953-4220-8bab-f0dc9d87de5e" />

### SAMPLE OUTPUT:

<img width="1600" height="1372" alt="image" src="https://github.com/user-attachments/assets/53e1d756-9790-4f28-8557-9603c8b8c1fe" />


# RESULT:

Thus, the linear convolution of the two given sequences were performed and its result was verified.
