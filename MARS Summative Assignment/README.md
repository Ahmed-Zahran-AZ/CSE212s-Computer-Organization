# MARS Project:
## Mathematical background
- Solving a first order ordinary differential equation numerically using Euler's method.
- A unique equation is assigned to each student, my equation is:
$$y'\ =\ 595x^3\ -\ 90x^2\ +\ 72x\ +\ 197y^2\ -\ 82y\ +\ 51$$
- One of the methods used to solve those equations numerically is euler method, which finds the value of y at any value of x by the following iterative algorithm:
$$y(x_{n+1}) = y(x_n)+h.F(x_n,y(x_n))$$
$$x_{n+1} = x_n +h$$
Where:
- $h$ is the discrete step size in x-axis
- $x_n$ and $y(x_n)$ are values of $x$ and $y$ at the step $n$
- $x_{n+1}$ and $y(x_{n+1})$ are the values of $x$ and $y$ at the next step
Algorithm starts by setting $x_n = 0$ and $y(x_n) = y(0)$ , then iteratively reaching $y$ at any given $x$ 
## Requirements
- Write an assembly function with the name “euler_fn” that solves the first order ODE
- The function will take inputs (using `pa` option):
    - $y(0)$
    - $h$
    - The required number of steps 
-  The function returns $y$ as output.
- The returned value should be kept in `$v0` and written in memory address `0x1001 0000` (first data address in MARS)

## Evaluation:
- pseudo-instructions or extended instruction formats are not permitted 
-  Main evaluation criterion is the correctness of the functionality. i.e., the value stored in memory and returned values.
- 