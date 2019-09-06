
# Blog 0 (September 6, 2019)

### CIT160 Lab and small issues

So the first thing I did was to start the CIT160L assignment to get Docker ready and installed. However while traversing through the assignment, there was one part that gave me trouble for around 30 mins. 

The Trouble: 
![Trouble](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/cit160%20lab%20errors.png?raw=true)

The first two commands did not give me issues too much, created the `etc` directory then navigated to it. Simple
```
$ mkdir cit160/etc
$ cd cit160/etc
```

The third command was giving me the error, and in hindsight I did something wrong in a very stupid way.
```
$ scp <UID>@ssh.sandbox.csun.edu:~steve/cit160/etc/dockerfile .
```	

The thing I did wrong was when ran the command, out of habit when reading a command, I replaced `~steve` with my own username.  Since I did got it to work, I can say that it was just poor knowledge and overlooking the bash command. 

And so after trying multiple times, I consulted a friend who had taken this specific class the previous semester and he told me to simply type it verbatim, which worked perfectly. If I had read the instructions more carefully, I would understand that the only time I would have ever needed to supply any of my own information was when I saw the `<USER>` part appear. 

### Creating this webpage and using Jekyll/Markdown


Just testing to see how this looks for now
