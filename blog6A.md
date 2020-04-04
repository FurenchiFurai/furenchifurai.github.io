# Blog 6A (March 13, 2020)

### Topic - Salt and Hashing

So if you remember blog 8 from last semester, I talked about SSH and encryption and mentioned hashing. Since I ran out of hardware topics off the top of my head, I will talk about salting combined with hashing.

So just to have a brief overview of what hashing is, then message is sent through a function that creates the same output every time your run that message through the fuction. If any part of the message is changed, then the output of the function will change. This is very secure since you must know the **exact** message to be able to replicate the output and the output is not reversible, meaning it is impossible to get the message from the output of the function alone.

#### What is password hashing?

So like stated above, hash algorithms are one way functions, meaning that any change in the original input will give a completely different output

i.e.
```
hash("hello") = 2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824
hash("hbllo") = 58756879c05c68dfac9866712fad6a93f8146f337a69afe7dd238f3364946366
hash("waltz") = c0e81794384491161f1777c232bc6bd9ec38f616560b120fda8e90f383853542
```

Notice how changing a single letter in the word "hello" changed the entire ouput.

Why is this good? Because to protect user accounts, we must have a method that can store passwords in a way where if any point the password file is compromised by a malicious attempt, they would not be able to find out the passwords of the users (easily)

For example, a user creates a new account. The password that they created got hashed by a function and stored into a database for safekeeping. During login attempts, the entered password is hashed then checked against the stored hash to see if it matches. If they match, then the user will have access. 

This same concept is why when you go to different sites to download files, they usually have the hash of the file shown on the page. This is to ensure that in no point their systems were compromised and a different file was created instead. Users can download the file, and hash it to see if it matches before they do anything important with the file.

Common secure hash functions are SHA256, SHA512, RipeMD and WHIRLPOOL

#### Issues with hashing

Hash functions are ingenious and strong, however they are not unbeatable. Above, I stated that if the input changes any bit, then the entire output is different too. However, there are a limited amount of characters that can be placed together and still be unique (even though it looks endless, if we created a cap on the length of the input, then there will be a cap on the length of possible combinations)

Because of this, there are 2 methods that are very popular in cracking hashes: *dictionary and brute force attacks*.

The *dictionary* method basically uses common types of password combinations and hashes them compares them. Usually these attacks are pulling from large files or even real password databases. Some examples are "h3110" for "hello" or "s3cr3t" for "secret". Currently depending on the site, I do not believe this method is as strong since most sites require symbols added into the equation, which can mess with the current dictionary (assuming they only use numbers and letters)

More dictionary examples:

```
Trying apple        : failed
Trying blueberry    : failed
Trying justinbeiber : failed
...
Trying letmein      : failed
Trying s3cr3t       : success!
```

The *brute-force* method basically takes all possible combinations up to a specified length and tests them. This method encompasses much more variety of passwors, however takes exponentially longer and is the least efficient but will usually find the password. Some examples are like "000" "001" "002" etc.  Currently this method on sites are really difficult to pull off, since many sites have preventative measures that lock the account after a certain number of tries (5 - 10) so there is no way to try every possible combination with this method.

More brute-force examples:

```
Trying aaaa : failed
Trying aaab : failed
Trying aaac : failed
...
Trying acdb : failed
Trying acdc : success!
```

However, there is a different method that combines both dictionary and brute-force method: *lookup tables*

The basic premise, is common password styles are hashed and stored alongside their input into a database. This lets the program compare the hashes, find the matching one and then just enter the password that is associated with that hash to gain access.

i.e.

```
Searching: 5f4dcc3b5aa765d61d8327deb882cf99: FOUND: password5
Searching: 6cbe615c106f422d23669b610b564800:  not in database
Searching: 630bf032efe4507f2c57b280995925a9: FOUND: letMEin12
Searching: 386f43fab5d096a7a66d67c8f213e5ec: FOUND: mcd0nalds
Searching: d5ec75d5fe70d428685510fae36492d9: FOUND: p@ssw0rd!
```

#### What is salting?

As I showed above, hashing is strong however is still can be beat, so what is something that can help mitigate that: salting.

So basically you just add salt and you are done.

(just kidding, kinda)

Salting is the basically adding a random string of characters to the end of the input which would, as stated above, change the whole output. This changes how the password is checked, so usually the salt is stored with the hash to be computed. This also mitigates the issue of multiple users having the same password since the salts are usually randomized meaning the added characters will create a different hash output for the same password (genius option).

i.e.

```
hash("hello")                    = 2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824
hash("hello" + "QxLUF1bgIAdeQX") = 9e209040c863f84a31e719795b2577523954739fe5ed3b58a75cff2127075ed1
hash("hello" + "bv5PehSMfV11Cd") = d1d3ec2e6f20fd420d50e2642992841d8338a314b8ea157c9e18477aaef226ab
hash("hello" + "YYLmfY6IehjZMQ") = a49670c3c18b9e079b9cfaf51634f563dc8ae3070db2c4a8544305df1b60f007
```
