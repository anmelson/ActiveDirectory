# Active Directory

A project designed to expand working knowledge of Active Directory.

## Description

The goal of this project is an in depth look into the functions and features of Active Directory, along with a lab implementation component.   

## Languages and Utilities Used

- **Microsoft Active Directory**

## Program Walk-through

### To begin, we take the role of someone at the Help Desk who has just recieved the following email

![Received Email](https://i.imgur.com/Cw4b8F4.png)

### We were tasked with adding three users to IT using first and last name, first initial.last name for the logon, and a forced password reset

![User Example](https://i.imgur.com/CpYxLkJl.png)
![Users Added](https://i.imgur.com/Crg5OYyl.png)

### Next, two users with inactive accounts had to be removed.  Using the find command, I searched for and removed the users

![Find for Deletion](https://i.imgur.com/eOYVI5Cl.png)

### A user had been locked out of their account for too many password attempts, so I found them with the find command and reset their password and unlocked their account

![Account Unlock](https://i.imgur.com/rGMY2VSl.png)

### I needed to create a new Organization Unit for the three users I had created prior

![New OU](https://i.imgur.com/tYxuMHOl.png)

### Nested within that OU needed to a be a group with the same name, 'Security Analysts'

![Nested Group](https://i.imgur.com/EEMdQ2Ql.png)

### The three users were moved into the new OU, and added to the nested Group

![Moved Users](https://i.imgur.com/eAvfSDJl.png)

### Nexy I needed to make a copy of Logon Banner GPO and rename it for the new group to enforce new permissions

![Copy of Logon Banner](https://i.imgur.com/PloFzajl.png)

### The copy was renamed, and applied to the group I had created earlier

![Applying the GPO](https://i.imgur.com/JrchWkPl.png)
![Applying the GPO](https://i.imgur.com/TtHuBBal.png)

### The new permissions required deny all to any removeable media devices

![Denying Access to Removeable Media](https://i.imgur.com/fzig5zDl.png)

### They required access to the command line to perform their work duties

![Command Line Access](https://i.imgur.com/JtIdDrDl.png)

### I needed to ensure that the Logon display was copied over from Logon Banner, which it was

![Logon Display](https://i.imgur.com/FNzyoQ4l.png)

### Finally, this group required specific password policies, so I went in and adjusted those to match the requirements

![Updated Password Policies](https://i.imgur.com/niMRLdul.png)

### For the last goal I needed to add a computer to the domain

![Adding the computer](https://i.imgur.com/UnoFvuwl.png)
![Adding the computer](https://i.imgur.com/uVb5VFMl.png)

### Success

![Success](https://i.imgur.com/Y4euMJRl.png)

### And lastly, move the new added computer into the correct OU which we made earlier

![Moved computer to new OU](https://i.imgur.com/aKOmQbkl.png)

## Conclusion

This Active Directory project provided a deep dive into the key functions and roles AD plays in enterprise settings. From managing users and setting up organizational structures to enforcing stringent security policies, I gained hands-on insights into the multifaceted nature of AD.

Challenges, like aligning specific user permissions and ensuring correct policy applications, emphasized the precision and understanding required in IT administration. It highlighted the strategic importance of AD in ensuring a streamlined and secure organizational workflow.

What resonated the most was seeing AD in action, reinforcing its crucial role in daily IT operations. It's more than just a tool; it's the backbone of many organizational processes, dictating access, security, and functionality.

In summary, this journey was an enlightening venture into the core of IT infrastructure management, strengthening my grasp on the intricacies of Active Directory.
