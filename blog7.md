# Blog 7 (October 25, 2019)

### Blog Changes

So, after presentations last week, the class was notified to improve the quality of their blogs by talking about more technical things instead of it being a diary. So I will be talking about topics that I learned/learning/researching throughout the week 

New structure will just be about the Topic that was learned, and hopefully like a half-wiki and thoughts.

### Topic: LDAP

So since I am in the CIT496 class, where I was on a team whos project was creating an LDAP server and being able to query users and then trying to implement a translucent proxy overlay. 

#### What is LDAP? 

Basically, LDAP stands for **L**ightweight **D**irectory **A**ccess **P**rotocol) and is a software protocol that allows people of an organization to locate individuals and devices in a network.  

At CSUN, if anyone has used a campus computer, they have authenticated through LDAP. 

For our project, we used OpenLDAP, which is a open-sourced version, which we used to test alot of our configurations for our project. 

#### Most used commands for OpenLDAP/LDAP?

From my research and testing, I found that the most common commands used were 
`ldapadd`, `ldapmodify`, `ldapdelete`, and `ldapsearch`.  Keep in mind, I am a pretty green user of LDAP, and this was a very basic LDAP server that I was working on. 

##### ldapadd

ldapadd is the command used to add content into your LDAP server.  The content is added through a `.ldif` file and must contain specific attributes for the user to be created. As an example, the following picture is one I did for our professor of CIT496, Adam Kaplan
![ldapadd](https://github.com/FurenchiFurai/furenchifurai.github.io/blob/master/ldapadd.png?raw=true)

##### ldapmodify

ldapmodify is the command used to modify existing entries in your LDAP server. This command could be done with or without the `.ldif` file and can also be used to delete entries as well.  This was one of the more rare commands, but still is prevalent when using it with the translucent proxy.

##### ldapdelete 

ldapdelete is the command used to delete exiting entries in your LDAP server.  From my experience, I only used this command a handful of times because I never really needed to delete the test users I was creating. However, the deletion does have a rule where if an entry is a "parent node", it cannot be deleted without deleting all child entries/nodes first. 

##### ldapsearch

ldapsearch is the command used to query up entries on the LDAP server, and can filter out specific attributes on entries.  This was my most used command since I mainly used the majority of it to make sure the entries were being added/modified correctly

