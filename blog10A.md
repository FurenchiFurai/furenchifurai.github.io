# Blog 10A (April 17, 2020)

### Topic - Active Directory

Another week, another blog. Funnily enough, you would think that during this StayAtHome orders for everyone, I would be learning more things to write about, but thats not the case so I will be talking more about some things I learned in Office 365 training at work. As stated in the title, I will be talking about Active Directory, a key component of a many corporations and organizations. While my knowledge is very basic, it should be enough to explain some things about it. 

#### What is Active Directory?

So starting off with a definition from [jumpcloud.com](https://jumpcloud.com/blog/active-directory-faq) "Active Directory is a directory service that enables administrators to manage and secure their IT resources. AD stores information about network objects (e.g. users, groups, systems, networks, applications, digital assets, and many others) and their relationship to one another. Admins can use AD to create users and grant them access to Windows laptops, servers, and applications. They can also use AD to control groups of systems simultaneously, enforcing security settings and software updates."

Active Directory, as part of its name, is a directory service from Microsoft which shows the relationships of objects on your organization's network. This helps administrators keep track of users and groups and other digital assets that are tied to specific users which helps them keep track of all the activity for that user/device. 

![activedirectory](https://130e178e8f8ba617604b-8aedd782b7d22cfe0d1146da69a52436.ssl.cf1.rackcdn.com/active-directory-security-essential-defenses-showcase_image-3-a-12828.jpg)

In most cases, AD is usually a part of IAM (Identity Access Management) and is aided by SSO (single sign-on) and/or MDM (mobile device management) as security add-ons for organizations which allow personal devices and want to manage them in a more secure way.

Last semester, I talked about LDAP and its uses. Active Directory uses LDAP as a protocol alongside the DNS protocol which allows Active Directory to freely add/delete/modify/search anyone/anything in the organization. And as stated in the name, it is "active" meaning that any changes to any object will be reflected throughout the system and all servers after a couple of minutes. This happens at a regular timeframe so information stays updated and is synced. 

Unknowingly most people (who are on Windows at their workplace) use Active Directory every day, as the primary sign in method to access their devices and files.

![domainlogin](https://www.tenforums.com/attachments/tutorials/228599d1553616873-enable-show-local-users-sign-screen-domain-joined-windows-10-a-domain_sign-in_windows_10.jpg)

#### Common terms and Azure AD

To get familiar with Active Directory, you must know the terms used when talking about Active Directory, here are a few of the most common ones.

**object**
- generic term of any unit of information (user, device, server etc.)

**groups**
- a set of multiple objects managed with permissions, changes to group are made on all objects under group

**domain**
- a collection of users, computers and device using the same active directory database

**tree**
- a collection of domains, i.e. a domain in Los Angeles and a domain in San Francisco could be part of a California tree

**forest**
- a collection of trees, domains and objects, i.e a California tree and New York tree can be part of the USA forest

**domain controller** 
- any server running Active Directory Domain Services (method to setup a database and relations). When trying to access objects in hte database, users will authenticate and be granted permission or denied access depending on their permission level in Active Directory.

![azuread](https://docs.microsoft.com/en-us/azure/active-directory/cloud-provisioning/media/what-is-cloud-provisioning/architecture.png)

While Active Directory is still commonly used, there is a new option with the rise of cloud services becoming more popular: **Azure Active Directory**

The biggest misconception of Azure is that most people think is is Active Directory on the cloud, it is actually an extension of an existing Active Directory instance on the cloud. This just adds on to functionality as any cloud resources can be accessed similarily to how current resources are accessed through the domain controller.
