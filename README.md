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