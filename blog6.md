# Blog 6 (October 18, 2019)

### Finishing up Group Project 0 again, with more obstacles

Continuing from last week, since we had a extenstion on the first group project, our group was able to finalize some extra things we wanted to do for our project.  Some things did change however, such as the switch from Centos to Ubuntu for the webserver which means a different playbook with different tasks since it using a different OS.

This was not too difficult, compared to last week with Centos, but apparently it was because of a specific version that caused all the issues.  For some reason, on Docker, if the container is using an instance of `centos:latest` then they will get Centos 8.  Which for some reason messes up and has to go through that snippet of code that Professor Lisa showed me in `blog5`.  I decided to test everything else in using an image of Centos 7 and that removed all the hassle, since everything seems to work perfectly fine on 7 and does not even need the snippet of code to install Ansible.  

Our group also decided that I should be the one to do the TLS/SSL stuff for the webserver automatically, so I had to use Ansible to modify some configuration files in each respestive OS and enable some security modules so that our webserver can see on port 443.  This was also a little of pain, since both were completely different methods, and I had to create 2 seperate VM's to test how it would look on a site. 

As of writing this, our team is still polishing up the playbook since it is still bugging out and we do not want to commit it to our webserver before it fully works.

### Other things during the week

Mainly alot of my time this week was spent on the group project doing research for this project and some other research for my other group presentation. The free time I had left was mainly to just relax from the research and work with YouTube videos and videogames