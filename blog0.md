
# Blog 0 (September 6, 2019)

### CIT160 Lab and small issues

So the first thing I did was to start the CIT160L assignment to get Docker ready and installed. However while traversing through the assignment, there was one part that gave me trouble for around 30 mins. 

The Trouble: 
![Trouble](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/images/cit160%20lab%20errors.png?raw=true)

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

Surpsingly I thought this part was going to be the most difficult to achieve, but after fiddling with tutorials and the settings in the repository and creating/deleting some failed ones I was able to get Jekyll to work on the page.

What I found easiest to do, was to simply create the repository which would be to use `<username>.github.io` as the repository name and then head off from there. 

Then head to your settings for that specific repository, and scroll down to **Github Pages** section and you are able to choose a theme that works, which in my case chose *Slate* and all markdown pages `.md` should automatically import the configuration settings from the `_config.yml` file. From there, you can populate the repository with your files to show online.

Unfortunately, while I was doing this, I accidentally set my [README](https://furenchifurai.github.io) to be the mainpage of my site, so for the time being, I'll keep that until I find a fix for it in the near future. 

***This is my first time writing a blog post, so I am not sure if there are things needed to be added/removed and whether this is too short/long***