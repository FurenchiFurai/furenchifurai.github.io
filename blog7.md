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



