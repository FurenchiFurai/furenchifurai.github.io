# Blog 5 (October 11, 2019)

### Finishing up Group Project 0, with some difficulty

So this week we did not have a lab to do since our project 0 is going to be due this week on Saturday but there was some enviromental issues that caused a little hitch, and so this project is extended a week.  My condolences for those who lost friends/family/possessions to the fire that happened in Sylmar.

However before this unfortunate event, I was working on my portion of the project, which was to create an ansible playbook to install a webserver (Apache) that shows a generic `index.html` page that lists the members of our team and our team name. 

I was building this playbook separately and testing it on a CentOS 8 instance through Docker.  This was where alot of issues were created as I had a very difficult time getting `ansible` on my instance for some reason.  All the normal methods of just doing `yum install ansible` were simply not working and after a couple days, I decided to talk to our professor to see if she knew how to get it working.  After some chat about what I did, and some things she asked me to do, a snippet of code was sent that fixed the blockage and helped me get `ansible` on my Docker instance.

This was the snippet:
```
yum makecache --timer
yum -y install epel-release initscripts
yum -y update
yum -y install sudo
yum -y install python3
yum -y install python3-pip
yum clean all
pip3 install ansible
sed -i -e 's/^\(Defaults\s*requiretty\)/#--- \1/'  /etc/sudoers
ansible --version
```
From what I could understand, some packages were installed, and using `pip3` to install `ansible` then giving permissions in the `/etc/sudoers` to have ansible run as `root`

### Other things during the week
