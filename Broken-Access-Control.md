# Broken Access Control 

![image](https://github.com/vsang181/OWASP-Interview-Preperation/assets/28651683/29143851-e048-4420-910f-4df14839ecc4)

Broken access control is a significant vulnerability in web application security, where users can exploit flaws to gain unauthorized access to sensitive data or perform actions beyond their intended permissions. It's crucial to understand its intricacies for interviews or real-world scenarios. 

## Definition 

Access control mechanisms enforce policies dictating what actions users are permitted to perform within an application. When these mechanisms fail, unauthorized users may gain access to restricted functionalities or data, leading to potential breaches. 

## Common Issues 

The OWASP report highlights several common access control vulnerabilities, including-  

- Inadequate enforcement of the principle of least privilege. Giving too much access to everyone instead of only to those who need it. 
- Bypassing access controls through URL manipulation or session tampering. Changing the website address or using special tools to get into places you're not supposed to. 
- Insecure direct object references.  Looking at or changing someone else's account just by knowing its special code. 
- Missing access controls on API endpoints. Using certain parts of a website without the proper controls in place. 
- Enabling Privilege escalation. Pretending to be someone else without permission, like an admin or another user.  
- Metadata Manipulation. Messing with important information like access tokens or cookies to gain more power. 
- CORS misconfiguration. Making a mistake in setting up who can use certain parts of a website through the internet. 

## Mitigation Strategies 

To mitigate broken access control vulnerabilities, developers should implement the following- 

- By default, say no to access unless it's a public thing. 
- Use access controls in one place and use them again and again across the website. Be careful with how different websites share resources. 
- Make sure people can only mess with their own stuff, not anyone else's. 
- Make sure the website sticks to the rules set by the business, so it doesn't go off track. 
- Hide important files and make sure the server doesn't show a list of what's there. 
- Keep track of when people try to get into things they're not supposed to, and tell the admins if it happens a lot. 
- Put a limit on how much someone can mess with the website at once, to stop them from causing too much trouble. 
- When you log out, make sure the server forgets who you are. For special tokens that don't need remembering, make them only last a short time. If they need to last longer, follow certain rules to make sure they can be stopped if needed. 

> Scenario 1: The application doesn't check if the account number sent by the user is valid before using it in a SQL query to fetch account information. So, an attacker can change the account number in the URL to access any user's account if it's not properly checked. 

``` 
pstmt.setString(1, request.getParameter("acct")); 
 ResultSet results = pstmt.executeQuery( ); 
``` 
``` 
https://example.com/app/accountInfo?acct=notmyacct 
``` 

> Scenario 2: If a regular user can access the admin page or any sensitive page without the right permissions, that's a problem. Admin rights should be required to access admin-related pages. 

``` 
https://example.com/app/getappInfo 
https://example.com/app/admin_getappInfo 
```

## Categories

- [Authorization](Authorization.md)
- [Insecure Direct Object Reference](Insecure_Direct_Object_Reference.md)
- [Transaction Authorization](Transaction_Authorization.md)
- [Cross-Site Request Forgery](Cross-Site-Request-Forgery.md)

## Let's Connect

I welcome your insights, feedback, and opportunities for collaboration. Together, we can make the digital world safer, one challenge at a time.

- **LinkedIn**: (https://www.linkedin.com/in/aashwadhaama/)

I look forward to connecting with fellow cybersecurity enthusiasts and professionals to share knowledge and work together towards a more secure digital environment.
