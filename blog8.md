# Blog 8 (November 1, 2019)

### Topic - SSH

Since it is one of the most common tools used in industry to do any work remotely, I will be talking about **SSH** today.

#### What is SSH

So doing a quick Google search will give you a [wikipedia article](https://en.wikipedia.org/wiki/Secure_Shell) that states the history of the tool. But the given definition is "a crypotgraphic network protocol for operating network services securely over an unsecure network". Sinmply put, a tool used to access secure resources 

The first instance most CSUN CIT students will have of this would be in CIT 160 where they are tasked to SSH into a server and run a few bash commands on the command line.  They would connect to a server using the command `ssh <server name>` through port 22.

#### How to use it?

```
ssh <user>@<host/server>
```
There are 3 parts
- `ssh` start off and tells your system to open the Secure Shell Connection
- `<user>` would be the account that is trying to access to (i.e. root) which would have their own permissions on the remote server that you are trying to connect to
- `<host/server>` is the computer/server/ip-address/domain you are trying to remotely access

Once you run the command with the preferred values, the system will prompt you to authenticate with a password for that user (if exists)

#### How secure is it?

Well since its an industry standard to this day, I would say it is but what methods do they use?

SSH has 3 forms of encryption (a way to hide something so it is hard to decipher) that it uses.
- Symmetric Encryption 
- Asymmetric Encryption
- Hashing

##### Symmetric Key Encryption

This method uses a shared secret or key between the client and host machines.  Basically the key is used to encrypt and decyrpt the message sent between the two machines. This key is only shared between the two communicating machines and is not shared to any outside party. This method is the primary form used to communicate.

How is the symmetric key generated? Well there is an algorithm called the Diffie-Hellman Key Exchange, where some simple math is done using prime numbers and an encryption algorithm (i.e. AES aka Advanced Encryption Standard). However this will be explained as next week's topic :)

##### Asymmetric Key Encryption

Contrary to the last method, this method uses 2 key pairs, one public key and one private key, aka the public-private key pair.  Each key has a different function, one encrypts and sends out the message, while the other decrypts the message received. The public key would be shared to a trusted source and the source would encrypt a message using that public key. The message then would be sent back to the public key owner, and the encrypted message is then decrypted using the owners private key. 

This encryption method is used to securely send the symmetric key (from above) to extablish a secure connection.

##### Hashing

The final method of encryption is not used for any form of communciation but used to test the authenticity of the message.  Basically the message goes through an irreversible function that always creates the same output. If any part of the input is changed, even by 1 bit, then the whole output is changed. 

The message will usally be sent with the hash, and the receiver can determine whether the message was tampered with or not by running the message through the same hashing function and comparing the outputs.