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

#### Example 1, 2 Variable Equation

So for the first example we have **R = AB + !AB**

![kmap3_ex1A](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1A.png?raw=true)

We see that there are 2 variables, **A** and **B**, therefore the next step is construct a truth table. The truth table just gives the location of the of the **1's** in the K-Map

![kmap3_ex1B](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1B.png?raw=true)

The K-Map, showing that value of (A,B), i.e. (0,0) is **0** while (0,1) is **1** in the K-Map grid.
From there the **1's** are grouped, and in this case the largest and most efficient option is the rectangle shown. Then the grouping is simplified, it shows that the value of **B** is the simplication of the equation.

![kmap3_ex1C](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1C.png?raw=true)
![kmap3_ex1D](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex1D.png?raw=true)

This is true since if you do the algebraic method, you would factor out **B**, getting **B(A+!A)** which would also be **B** as well. 

In this case, it was simple enough so there is one solution, but bear in mind that with larger equations, depending on how the grouping was done, there could be multiple different solutions. 

#### Example 2, 3 Variable Equation

So for the next example, we have **R = !A!B!C + !A!BC + !ABC + !AB!C + A!B!C + AB!C**

![kmap3_ex2A](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex2A.png?raw=true)

We see 3 variables, **A**, **B**, and **C**, therefore the next step would be to create a truth table. Lets have a random output that looks like this:

![kmap3_ex2B](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex2B.png?raw=true)

From this, a K-Map is constructed, where **A** is on the X-axis and **BC** is on the Y-axis with the values for each part of the grid filled in according to the values of the truth table

![kmap3_ex2C](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex2C.png?raw=true)

From this we start grouping, and the best options are to group the entire top row and group the external columns (wrap around rule). They are factors of 2 (both are 4 items each).  From this we can deduce that the rectangle row is **!A** and the square created from the 2 external columns would be **!C**. So the final solution is **R = !A + !C**

![kmap3_ex2D](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex2D.png?raw=true)

#### Final Example, 4 Variable Equation

For this case, we have this equation:

![kmap3_ex3A](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex3A.png?raw=true)

We see 4 variables, **A**, **B**, **C** and **D**.  In this case we are going to have the K-Map with the values displayed on it already, so we do not need to construct a truth table.

![kmap3_ex3B](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex3B.png?raw=true)

From here, we do the grouping and the most efficient method I saw that works is for the corners to be grouped (this wrap method looks like a diagonal, but technically they wrap like a sphere). Second grouping is the first 2 values on the top and bottom rows to make a square. And the last grouping would be the top 2 of the last column. This yields a grouping that looks like this:

![kmap3_ex3C](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap3_ex3C.png?raw=true)

From these groupings we can conclude that  