# Blog 3 (September 27, 2019)

### Finishing Lab 2 and being ignorant

So, over the course of the last class and the weekend, I was finishing up Lab 2 where my playbooks were basically done just needed some fine tuning for them to work.  With some tutoring from my friend, Marcin, I was able to understand how a little more of the Ansible syntax.  

However, in the second playbook, we were tasked to do a LAMP stack through Ansible, and after configuring a large majority of the playbook, it was tested and always failed. The error was within one of my lines of code where I added the timezone function to make it so PHP could run.  

After about 5 hours of testing the playbook over and over (I probably made around 10 - 15 docker containers to do this), I saw that removing the option of the timezone made the playbook run and that when looking through the files, after running it actually adds the timezone directory.  But for some reason, trying to `curl` my localhost through my own terminal would never work or show the page.

After doing some more testing, I consulted the instructor and came to find out that there is no need to specify the timezone because Ansible has it own method of finding out and that I was supposed to `curl` the localhost through the container terminal instead of my host machine _facepalm_ 

This was the largest learning experience as I could see how much more I needed to learn to do something simple as a LAMP stack with automation

### Lab 3 and its intricacies

This is probably gonna be a shorter paragraph since I did not have that many issues with Lab 3, but I will elaborate on the part that did give me the most problems.

### Other things that happened throughout the week

More games 
