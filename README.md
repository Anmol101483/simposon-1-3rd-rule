
Name-Harshad Ainapure
Roll No. SEL69
Date-03/04/25
Exp No-06

Input-

"program for simpson's 1/3rd rule"
import math

def f(t):
    return(4-4*math.exp(-5*t))

a=float(input("Enter the lower limit\t"))
b=float(input("Enter the upper limit\t"))
n=int(input("Enter the no. of sub intervals\t"))

h=(b-a)/(1.0*n)
s=0
i=0
while(i<=n):
    if(i==0):
        s=s+f(a)
    elif(i==n):
        s=s+f(b)
    elif(i%2==0):
        s=s+2*f(a)
    else:
        s=s+4*f(a)
        
    a=a+h
    i=i+1

intg=h/3*s

print("The value of current is ",intg)

Output-

Enter the lower limit	0
Enter the upper limit	0.1
Enter the no. of sub intervals	10
The value of current is  0.0852245168436549
