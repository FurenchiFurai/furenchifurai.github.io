# Blog 9 (November 8, 2019)

### Topic - Diffie-Hellman Key Exchange

Resuming the topic from last week's blog, SSH uses multiple forms of encryption, and one method of of creating a secure channel is using the the **Diffie-Hellman Key Exchange** (DH). DH uses a simple math equation to generate a shared secret aka key to establish a connection between the two parties. This is significant as this key is never shared/transmitted but both parties are still able to generate the same key.

#### What is the process?

Lets say we have 2 people trying to communicate to each other, Alice and Bob

##### Step 1 - Base and prime
Both agree on a prime number, **_p_** and a base number **_g_** 

##### Step 2 - Mirrored equation 
Alice will choose a random (large) number called **_a_** and compute the equation
![bigA](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/blog9_bigA.png?raw=true)
She will send Bob the value **_A_**

Bob will choose a random (large) number called **_b_** and compute the same equation
![bigB](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/blog9_bigB.png?raw=true)
He will send Alice the value of **_B_**

##### Step 3 - Mirrored key equation
Alice will now use **_B_** to compute the equation
![keyA](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/blog9_keyA.png?raw=true)
She will get value **_S_**, which will be the key

Bob will now use **_A_** to compute the equation
![keyB](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/blog9_keyB.png?raw=true)
He will get value **_S_**, which will also be the key

We do this in an example (below), and you can see that both values of **_S_** are the same
![example](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/blog9_example.png?raw=true)

