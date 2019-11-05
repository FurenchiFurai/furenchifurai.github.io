# Blog 9 (November 8, 2019)

### Topic - Diffie-Hellman Key Exchange

Resuming the topic from last week's blog, SSH uses multiple forms of encryption, and one method of of creating a secure channel is using the the **Diffie-Hellman Key Exchange** (DH). DH uses a simple math equation to generate a shared secret aka key to establish a connection between the two parties. This is significant as this key is never shared/transmitted but both parties are still able to generate the same key.

#### What is the process?

Lets say we have 2 people trying to communicate to each other, Alice and Bob

Both agree on a prime number, **_p_** and a base number **_g_** 

Alice will choose a random (large) number called **_a_** and compute the equation
![]()
She will send Bob the value **_A_**

Bob will choose a random (large) number called **_b_** and compute the same equation
![]()
He will send Alice the value of **_B_**

