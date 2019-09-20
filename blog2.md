# Blog 2 (September 20, 2019)

### Lab 2, learning how to use Ansible

So I am one of the people that decided to do Ansible in Docker, and it is been a little hit or miss in terms of using ansible.  For starters, I was rushing a bit and was wondering why I could'nt use `sudo` , then realized that in the _the actual lab_ page it says that you need to install `sudo` to use it for Docker. **_facepalm_**


I found a handy [stackoverflow](https://stackoverflow.com/q/25845538) link to help me get this to work (I changed the ubuntu version to **latest** since that is what I was using)

Simply put:
```
FROM ubuntu:latest

RUN apt-get update && \
      apt-get -y install sudo

RUN useradd -m docker && echo "docker:docker" | chpasswd && adduser docker sudo

USER docker
CMD /bin/bash
```

Now the most difficult part was learning Ansible since I am not familiar with automation and I would have to learn the correct way to set up it up. 

I started with Playbook #2, since it was just lab1 but in ansible version, which should be relatively easier since the cloning can be done in a much simpler way.

I am partially done with my lab but there are so many things I still do not understand with the language and how it works that it makes it difficult to do things without testing frequently.

### Other things during the week

In my other class that I'm taking, CIT496P, the LDAP team that I am part is slowly making progress and from there we are able to actually learn how to use LDAP.  Our first sprint ends this coming Monday, and from there we have new tasks that we need to do to progress further in this project.  Its pretty fun so far seeing how things work and stuff.

As for my personal life, my uncle actually got me Borderlands 3, so in my spare time I have been playing that game, and its been pretty fun throughout. He originally got it for me to play with him, but ironically he has been too busy to even download it into his own computer. 

Also, one of the other games that I play alot is Destiny 2, and since there is an upcoming DLC coming to the game in the near future, the company has been putting out more info about the new features that is being implemented.  I'm really excited for that as well since its been one of my main games to play over the summer. 

**Picture of the DLC:**
![Shadowkeep](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/Destiny%202%20Shadowkeep.png?raw=true)

