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
From what I could understand, some packages were installed, and then using `pip3` to install `ansible`, then giving permissions in the `/etc/sudoers` to have ansible run as `root`

That fixed the installation of Ansible onto my instance, so then the rest of my job was to make sure I was able to get a LAMP stack running on CentOS (which on its own was a whole different monster, since we only did it with Ubuntu in a previous lab).  I am still currently working on it and testing as I go along.

### Other things during the week

This week was a bit different, a little more stressful with the project and another project from another class were being due on a simnilar timeframe, forcing me to delegate time to do one or the other, instead of focusing all of my time into one.  

Aside from all of this, during my "rest", I was catching up on some YouTube series and playing games to take my mind off of the projects.  Both games I play have had some QOL updates to them so I am really looking forward to having a full rest once these projects are done.