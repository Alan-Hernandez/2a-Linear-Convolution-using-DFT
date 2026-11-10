# EXPT 2a: LINEAR CONVOLUTION-USING-DFT
# AIM

To perform and verify linear convolution operation of two given sequences using SCILAB.

# APPARATUS REQUIRED 

PC installed with SCILAB

# PROGRAM:

# LINEAR CONVOLUTION

clc; 

clear;

x=[1 2 3 4];

n1=0:1:length(x)-1;

subplot(3,1,1);

plot2d3(n1,x);

xlabel('time');

ylabel('amplitude');

title('input sequence');

h=[2 4 8 6];

n2=0:1:length(h)-1;

subplot(3,1,2);

plot2d3(n2,h);

xlabel('time');

ylabel('amplitude');

title('impulse sequence');

N1=length(x);

N2=length(h);

N=max(N1,N2);

N3=N1-N2;

if(N3>0)

h=[h,zeros(1,N3)];

else

x=[x,zeros(1,abs(N3))];

end

disp(x)

disp(h)

for n=1:N

y(n)=0;

for i=1:N

j=n-i+1;

if(j<=0)

j=N+j;

end

y(n)=y(n)+x(i)*h(j);

end

end

disp(y)

n=0:N-1;

subplot(3,1,3);

plot2d3(n,y);

xlabel('time');

ylabel('amplitude');

title('circular convolution');

### CALCULATIONS:

<img width="704" height="1280" alt="image" src="https://github.com/user-attachments/assets/fe9d2cba-1aff-484a-a238-00c3c4ce12e7" />

<img width="792" height="1280" alt="image" src="https://github.com/user-attachments/assets/0a42a716-472a-4cbb-956d-b17e1d441235" />

<img width="648" height="1280" alt="image" src="https://github.com/user-attachments/assets/45d97bca-eaec-440d-acd8-5d09aa9e44d8" />

<img width="894" height="1280" alt="image" src="https://github.com/user-attachments/assets/ff238f0f-a953-4220-8bab-f0dc9d87de5e" />

### SAMPLE OUTPUT:

<img width="1600" height="1372" alt="image" src="https://github.com/user-attachments/assets/53e1d756-9790-4f28-8557-9603c8b8c1fe" />


# RESULT:

Thus, the linear convolution of the two given sequences were performed and its result was verified.
