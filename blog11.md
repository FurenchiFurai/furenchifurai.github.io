# Blog 11 (November 22, 2019)

### Topic - Karnaugh Map (K-Map) Part 2

So last weeks blog, we talked about basic Boolean Algebra where there are 3 main operators that are used: **AND**, **OR** and **NOT**.

Just to recap last week's blog, between 2 variables with values of 0 (false) and 1 (true)

The operators function as follows:
- **AND** requires both variables to be 1(true) or the outputs is 0(false)
- **OR** requires only one of the variables to be 1(true) or the output is 0(false) 
- **NOT** just flips the boolean value from 0(false) to 1(true) and 1(true) to 0(false)

Since not all operations or expressions are going to be basic, there should be ways to simplify when there are multiple variables with multiple operators. In this case, the first method of simplication/minimalization is through algebraic means, and the second method is K-maps, will be showcased next week.

#### Starting Off, why should there be circuit simplication?

As said last week, these operations are also used in circuitry to calculate output.  But why should we simplify these equations?

Like in programming, a longer program usually takes longer to execute, and that is also shared with long circuits. 

Bigger circuits usually equals bigger chippers which equals higher cost (exponentially)

Longer circuits equate to more time required for electrons to flow through, resulting in a slower execution.

From this, simplying boolean equations (circuits) makes it better for cost and effciency.

#### How to simplfy circuits

Suprising it is simple to regular algebra

Take for example the following expression: 

![kmap_ex1](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap_ex1.png?raw=true)

How would it be simplified? 

We would factor out **B**, then because **A + !A** is **A OR !A** the value will be 1(true) so we would end with B

![kmap_ex2](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap_ex2.png?raw=true)

Lets take another example:

![kmap_ex3](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap_ex3.png?raw=true)

From the first 2 variable sections, we factor out **BCD** and get **A + !A**, which we saw from before becomes 1(true). The output of this is now BCD from the first step.

From the second 2 variable sections, we factor our **B!CD** and also get **A + !A**, like above equals 1(true). The output of this is now B!CD from the second step.

We are now left with **BCD + B!CD**

From this, **BD** are factored out to get **C + !C** which like above equals 1(true), so therefore the result of the simplification is **BD**

![kmap_ex4](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/kmap_ex4.png?raw=true)

As you can see, doing this by hand could get very tiring and could also get very hard to track variables if there are many of them.  So we will be showing off the K-maps method which considerably makes this entire process simpler.
