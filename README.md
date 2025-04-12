# ✈ Hazrat Ali

# Programmer || Software Engineering 

# Eular Method : Number 1

# a=0;
# b=0.1;
# n=5;
# h=(b-a)/n;
# f = @(y,x) x + y;
# xi = @(i) a+i*h;

# x_not=a;
# y_not=1;
# while xi(x_not) <=b
   # y_not+=h*f(xi(x_not),y_not);
# x_not++;
# end;
# printf("%f", y_not);

# Simpson 3/8 : Number 2

# clc;
# clear all;
# a=0;
# b=1;
# n=6; %must be an even
# delX=(b-a)/n;
# f=@(x) 1/(1+x^2);
# xi=@(i) a+i*delX;
# sum = f(xi(0))+f(xi(n));
# i=1;
# while i<n
    if rem(i,3)==0
        sum += 2*f(xi(i));
    else sum+=3*f(xi(i));
    end;
    i++;
# end;
# sum*=((3*delX)/8);
# printf("%f",sum);

 # Simpson 1/3 : Number 3

# clc;
# clear all;
# a=0;
# b=1;
# n=6; %must be an even
# delX=(b-a)/n;
# f=@(x) 1/(1+x^2);
# xi=@(i) a+i*delX;
# sum = f(xi(0))+f(xi(n));
# i=1;
# while i<n
    if rem(i,2)==0
        sum += 2*f(xi(i));
    else sum+=4*f(xi(i));
    end;
    i++;
end;
# sum*=(delX/3);
# printf("%f",sum);

# Trapezoidal : 4

# clc;
# clear all;
# f=@(x) 1/(1+x^2);
# a=0;
# b=6;
# h=(b-a)/6;
# xi=@(i) a+i*h;
# sum=f(xi(0))+f(xi(6));
# i=1;
# while i<6
    sum+=(2*f(xi(i)));
    i++;
# end;
# sum*=(h/2);
# printf("%f",sum);

# Runge Kutta : 5

# clc;
# clear all;
# f=@(x,y)x+y^2;
# h=0.1;
# for_x=0.2;
# init_x=0;
# init_y=1;

# while init_x<for_x
   # k1 = h*f(init_x,init_y);
   # k2= h* f((init_x)+h/2,(init_y)+k1/2);
   # k3 = h* f((init_x)+h/2,(init_y)+k2/2);
   # k4 = h*f(init_x+h,init_y+k3);
   # init_y+=(1/6*(k1+2*k2+2*k3+k4));
   # init_x+=h;
# end;
# printf("%f",init_y);

# Hazrat Ali
# Software Engineer
# CSE 
# ID : 221010050
# 


