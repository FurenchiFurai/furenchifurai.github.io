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



#### Most common usage?

As stated before, the majority of CSUN CIT students first do this in one of their basic 100 level class, but this command has much more usage than that.