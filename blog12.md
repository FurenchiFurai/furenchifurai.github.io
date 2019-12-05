# Blog 12 (December 6, 2019)

### Topic - Karnaugh Map (K-Map) Part 3

Hope everyone had a good Thanksgiving.

The previous week's blog talked about simplification of Boolean algebra and showed 2 examples where the input is simplified through algebraic functions and then creates an output that is easier to use compared to the original expression. 

This week, we are going to learn of Karnaugh Maps, which is another way to simplify algebraic functions using a more picturesque method instead of a fairly computational way.

#### How to setup? And what are the steps/rules?

Rules:
- Groups must be **1**'s, be a multiple of 2 and can be overlapped
- Only adjacent grouping (wrapping around the map is permitted, diagonals are not)
- Groups must be largest possible and try to use the fewest amount of groups possible

*Reminder* that the K-Map can be grouped differently and comeup with a similar simplified expression.  This does not mean that one is right or wrong, but however it means that there is another valid simplication solution for the function


The current steps to start:
1. Review the function and see how many variables 
2. Construct a truth table (majority of the times, the output values will be given)
3. Construct a K-Map according to # of variables and output of truth table
4. Group efficiently
5. Simplfy solution 

#### Example 1, 2 Variable

So for the first example we have **R = AB + !AB**

![kmap3_ex1A](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1A.png?raw=true)

We see that there are 2 variables, **A** and **B**, therefore the next step is construct a truth table. The truth table just gives the location of the of the **1's** in the K-Map

![kmap3_ex1B](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1B.png?raw=true)

The K-Map, showing that value of (A,B), i.e. (0,0) is **0** while (0,1) is **1** in the K-Map grid.
From there the **1's** are grouped, and in this case the largest and most efficient option is the rectangle shown. Then the grouping is simplified, it shows that the value of **B** is the simplication of the equation.

![kmap3_ex1C](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1C.png?raw=true)
![kmap3_ex1D](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1D.png?raw=true)