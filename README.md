
## Matlab Basics
---
### Vectors

* simple


```octave
vec= [1 2 3 4 5 6]
```

    vec =
    
       1   2   3   4   5   6
    
    

* Another way to initialize vectors


```octave
vec =1:6
```

    vec =
    
       1   2   3   4   5   6
    
    

- 3rd way to init vec


```octave
vec = 1:2:10
```

    vec =
    
       1   3   5   7   9
    
    

>Difference between not giving ; or giving it

```octave
vec = 1:5

vec = 
    1  2 3 4 5
    
vec = 1:5;
### no output
```

## 2D matrix


```octave
A = [1 2 3 ;
     4 5 6;
     7 8 9
    ]
```

    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    

- other way to make matrix


```octave
A = [1:3;4:6;7:9]
```

    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    

## Operations on matrix

___
1. Transpose 
1. Inverse 
1. Addition 
1. Multiplication
1. To the Power n
1. Elementwise Operation
___
----


```octave
A
A_transpose = A'
```

    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    A_transpose =
    
       1   4   7
       2   5   8
       3   6   9
    
    


```octave
A
B=inv(A)
```

    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    warning: matrix singular to machine precision, rcond = 1.54198e-18
    B =
    
      -4.5036e+15   9.0072e+15  -4.5036e+15
       9.0072e+15  -1.8014e+16   9.0072e+15
      -4.5036e+15   9.0072e+15  -4.5036e+15
    
    


```octave
A
disp("<==================================Ans=======================>\n")
B = A + 6
C = A +B
```

    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    <==================================Ans=======================>
    
    B =
    
        7    8    9
       10   11   12
       13   14   15
    
    C =
    
        8   10   12
       14   16   18
       20   22   24
    
    


```octave
D = A * 2
e=[4:-1:2;3:-1:1;2:4]
#Mult with mat
E = A * e

```

    D =
    
        2    4    6
        8   10   12
       14   16   18
    
    e =
    
       4   3   2
       3   2   1
       2   3   4
    
    E =
    
       16   16   16
       43   40   37
       70   64   58
    
    

- To the power n


```octave
disp("A")
A
disp("A^2")
A_n=A^2
```

    A
    A =
    
       1   2   3
       4   5   6
       7   8   9
    
    A^2
    A_n =
    
        30    36    42
        66    81    96
       102   126   150
    
    

- ELementwise Operation Examples :
---


```octave
A 
A.*5
D
disp("eigen of D => ")
eig(D)
```

    A =
    
        1    2    3    4    5    6    7    8    9   10
    
    ans =
    
        5   10   15   20   25   30   35   40   45   50
    
    D =
    
        2    4    6
        8   10   12
       14   16   18
    
    eigen of D => 
    ans =
    
       3.2234e+01
      -2.2337e+00
      -2.6074e-15
    
    

In previous e.g. we are multiplying each element of **A** by **5**

The operator to doing element wise operation in matlab is 
```matlab 
 .*  # for multiply elementwise
 .^ # for to the power elementwise
```

E.g. 
```octave
A = 1:10
b = A .* 12
```


```octave
A = 1:10;
# Print in matlab
disp(A)
b = A .* 12
```

        1    2    3    4    5    6    7    8    9   10
    b =
    
        12    24    36    48    60    72    84    96   108   120
    
    

## Polynomial in Matlab
---
#### Matlab treats n+1 sized vectors as polynomila of n-th degree
- Example
---
>Polynomial => F(a) =  2*a^3 + 5*a +3 will be treated as :
```octave
 a = [2 0 5 3]
```

---
Now you want to know the value of the polynomial at a = 3. To do that the code :
```octave
 y = polyval(a, 2) # y(2) = 2*2^3 + 5*2 + 3
```


```octave
a = [2 0 5 3]
y = polyval(a,2 )
```

    a =
    
       2   0   5   3
    
    y =  29
    

### Matlab is so powerful
---
>Small Snippet to solve system of linear eq. 
```math-Equations
a1*x + b1*y + c1 = d1
a2*x + b2*x + c2 = d2
a3*x + b3*x + c3 = d3
```
```octave
A = [1 1 5; 1 5 1; 5 1 1]
b = [7;7;7]
X =  inv(A) * b # BOOM ; X => Solutions
```

---
Try it yourself


### Let's See how to take help about any function in matlab
>help function_name
```octave
help sin
```


```octave
help sin
```

    'sin' is a built-in function from the file libinterp/corefcn/mappers.cc
    
     -- sin (X)
         Compute the sine for each element of X in radians.
    
         See also: asin, sind, sinh.
    
    
    
    Additional help for built-in functions and operators is
    available in the online version of the manual.  Use the command
    'doc <topic>' to search the manual index.
    
    Help and information about Octave is also available on the WWW
    at https://www.octave.org and via the help@octave.org
    mailing list.
    

## UPCOMING Topics
- __STRING Formats__

 Link : [String Formats to print statements with variables included](https://in.mathworks.com/help/matlab/matlab_prog/formatting-strings.html)
- __Conditional Statements__
 * If-Else Structure 
     - link : [IF ELSE](https://www.tutorialspoint.com/matlab/if_elseif_else_statement.htm)
- __Loops__
 - while
>Syntax
>[While LOOP](https://in.mathworks.com/help/matlab/ref/while.html)     
 --- 
     
    ```
    while expression
        statements
     end```
     
  --- 
 - for
 
 >FOR LOOP Syntax
 
 ```octave
 #type 1:
 for i = start_index:end_index
     #body
 end
 #type 2:
 for i = start_index:steps_of_increment:end_index
     #body
 end
 #type 3:
 for i = start_index:steps_of_decrement:end_index
     #body
 end
 ```


```octave
#While LOOP
#Factorial
n = 10;
f = n;
while n > 1
    n = n-1;
    f = f*n;
end
disp(['n! = ' num2str(f)])  #display function with txt formating

#for Loop 1 inc Index
#Note: array starts from index 1
row=3;
col=4;
count=0;
H = zeros(row,col);
for r = 1:row
    fprintf("\nStep - %d\n",count++)
    for c = 1:col
        H(r,c) = r+c-1;
    end
    H
end

#for loop 2 Dec. Index
for v = 10:-1:1
   disp(v)
end
#for loop 3 : List
disp("Loop 3 ============================>")
for v = [1:2:10]
   disp(v)
end

```

    n! = 3628800
    
    Step - 0
    H =
    
       1   2   3   4
       0   0   0   0
       0   0   0   0
    
    
    Step - 1
    H =
    
       1   2   3   4
       2   3   4   5
       0   0   0   0
    
    
    Step - 2
    H =
    
       1   2   3   4
       2   3   4   5
       3   4   5   6
    
     10
     9
     8
     7
     6
     5
     4
     3
     2
     1
    Loop 3 ============================>
     1
     3
     5
     7
     9
    

### Let's See how string works in matlab 
> Link : [String Concats ](https://in.mathworks.com/help/matlab/ref/strcat.html)

```octave
a = ['Hello '];
b = ['World'];
strcat(a , b)
```

### User Input 
> Example
```octave
user_inp = input('Enter Your Name : ',user_inp)
```

# Thanks For Reading My First Matlab Basics
>Please Share this file with your friends

[Link to The Matlab Basics File](https://github.com/pmdproject2020/octave-files.git)

---
<img src="IMG_20181027_142507-01.jpeg"
     alt="No Image Found"
     style="float: center margin-right: 10px;" height="150" width = "200" ></img>
     
---     
&copy; Pritam Chakraborty \[31-01-2020\]
