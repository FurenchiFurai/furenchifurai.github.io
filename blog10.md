# Blog 9 (November 15, 2019)

### Topic - Karnaugh Map (K-Map) Part 1

#### What is a Karnaugh Map (K-Map)?

Basically put, it is a more visual method of solving Boolean algebra and is mainly used as utility for switching circuits. While its main function is for circuitry, because it is used to simplify Boolean algebra, it is still taught for basic knowledge of assembly. 

But before we go into K-Maps we must need to understand some Boolean algebra to use the shortcut.

#### Starting off, what is Boolean algebra?

So Boolean algebra according to [Wikipedia]() is a branch of algebra where the values are truth values `true` and `false` usually denoted as 1 or 0.

Equations uses multiple different operations with specific truth values to come to a generated output value.

There are 3 basic operations that Boolean algebra uses, **AND**, **OR**, and **NOT**

#### AND Operation

The **AND** operation is quite simple as it requires both variables to be the same in order to get a `true` value.

The **AND** symbol is usually a multiplicative dot, but because this blog is in Markdown, I am not able to simulate that symbol. So for now it will be an "**x**"

i.e.

`0 x 0 = 0` (Both values are false, therefore the output is false)

`0 x 1 = 0`	(Only one value is true, but both are not, so output is false)

`1 x 0 = 0`	(Only one value is true, but both are not, so output is false)

`1 x 1 = 0`	(Both values are true, therefore the output is true)

In electrical/computer engineering, the **AND** operator is also known as the **AND** gate

#### OR Operation

The **OR** operation is a bit different from the **AND** operation as it requires only of the variables to be the same to get a `true` value

The **OR** symbol is denoted as a **+** in operations

i.e.

`0 + 0 = 0`	(Both values are false, therefore the output is false)

`0 + 1 = 1`	(Only one value is true, only one is needed, so output is true)

`1 + 0 = 1`	(Only one value is true, only one is needed, so output is true)

`1 + 1 = 1`	(Both values are true, only one is needed, so output is true)

In electrical/computer engineering, the **AND** operator is also known as the **OR** gate

#### NOT Operation

