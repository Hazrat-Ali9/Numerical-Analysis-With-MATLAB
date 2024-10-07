# Eular Method 

a=0;
b=0.1;
n=5;
h=(b-a)/n;
f = @(y,x) x + y;
xi = @(i) a+i*h;

x_not=a;
y_not=1;
while xi(x_not) <=b
    y_not+=h*f(xi(x_not),y_not);
    x_not++;
end;
printf("%f", y_not);

# Simpson 3/8 : 

clc;
clear all;
a=0;
b=1;
n=6; %must be an even
delX=(b-a)/n;
f=@(x) 1/(1+x^2);
xi=@(i) a+i*delX;
sum = f(xi(0))+f(xi(n));
i=1;
while i<n
    if rem(i,3)==0
        sum += 2*f(xi(i));
    else sum+=3*f(xi(i));
    end;
    i++;
end;
 sum*=((3*delX)/8);
 printf("%f",sum);