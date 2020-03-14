# Blog 6A (March 13, 2020)

### Topic - Salt and Hashing

So if you remember blog 8 from last semester, I talked about SSH and encryption and mentioned hashing. Since I ran out of hardware topics off the top of my head, I will talk about salting combined with hashing.

So just to have a brief overview of what hashing is, then message is sent through a function that creates the same output every time your run that message through the fuction. If any part of the message is changed, then the output of the function will change. This is very secure since you must know the **exact** message to be able to replicate the output and the output is not reversible, meaning it is impossible to get the message from the output of the function alone.