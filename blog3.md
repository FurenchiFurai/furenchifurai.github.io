# Blog 3 (September 27, 2019)

### Finishing Lab 2 and being ignorant

So, over the course of the last class and the weekend, I was finishing up Lab 2 where my playbooks were basically done just needed some fine tuning for them to work.  With some tutoring from my friend, Marcin, I was able to understand how a little more of the Ansible syntax.  

However, in the second playbook, we were tasked to do a LAMP stack through Ansible, and after configuring a large majority of the playbook, it was tested and always failed. The error was within one of my lines of code where I added the timezone function to make it so PHP could run.  

After about 5 hours of testing the playbook over and over (I probably made around 10 - 15 docker containers to do this), I saw that removing the option of the timezone made the playbook run and that when looking through the files, after running it actually adds the timezone directory.  But for some reason, trying to `curl` my localhost through my own terminal would never work or show the page.

After doing some more testing, I consulted the instructor and came to find out that there is no need to specify the timezone because Ansible has it own method of finding out and that I was supposed to `curl` the localhost through the container terminal instead of my host machine _facepalm_ 

This was the largest learning experience as I could see how much more I needed to learn to do something simple as a LAMP stack with automation

The result of running `curl localhost` in the container
![curl localhost pb2](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/curl%20localhost.png?raw=true)

### Lab 3 and its intricacies

This is probably gonna be a shorter paragraph since I did not have that many issues with Lab 3, but I will elaborate on the part that did give me the most problems.

So going through the first part was pretty simple, just had to follow and type the commands needed verbatim to get things to work as intended.  Then starting the second part was little different since we had to attach mulitple ports to the container but was pretty straightforward after as it was doing the same thing as part 1 except we installed the Node Exporter of Prometheus instead of Prometheus. Then we had to edit the `prometheus.yml` file 

![prometheus edit](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/prometheus%20edit.png?raw=true)

Then the issue happened, it was supposed to let the host monitor the nodes after the `prometheus.yml` configuration was changed.  However in my case, I was not able to show the node option, but after some testing, I realized that you need to have both the prometheus running and the node exporter running at the same time (hence the need for another termminal window).  In hindsight that made complete sense, but I was stuck for a solid 30 mins trying to see if I did anything wrong. 

### Other things that happened throughout the week, and future stuff

Playing through Borderlands 3 is very fun and I just recently beat the game and now going through to fully complete it by doing all the side missions needed. On a little side note, this weekend is the finals for Overwatch League, which is coincidentally on Sunday, so the plan is to go to a friends house where we can all watch it together

Also this coming Tuesday is Destiny 2 Shadowkeep

Here is the trailer:

[![Destiny 2 Shadowkeep](http://img.youtube.com/vi/LFYJTudJ540/0.jpg)](https://www.youtube.com/watch?v=LFYJTudJ540 "Destiny 2 Shadowkeep")
