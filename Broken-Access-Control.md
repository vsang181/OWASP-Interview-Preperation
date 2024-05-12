# Broken Access Control

![BrokenAccessControl2](https://github.com/vsang181/OWASP-Interview-Preperation/assets/28651683/6df4eb7b-77f2-4cca-ba82-9316af696c9f)

Broken Access Control is a vulnerability in web application security, enabling unauthorized users to access restricted data or perform unauthorized actions. Understanding and addressing this vulnerability is paramount for securing web applications effectively.

## Definition

Broken Access Control occurs when access control mechanisms fail to enforce policies regarding user actions within an application. This failure leads to unauthorized access to sensitive functionalities or data, potentially resulting in security breaches.

## Common Issues

OWASP identifies several common Broken Access Control vulnerabilities, including:

- **Inadequate enforcement of the principle of least privilege**: Granting excessive access privileges to users instead of restricting access to only what is necessary.
- **Bypassing access controls through URL manipulation or session tampering**: Exploiting vulnerabilities to change URLs or tamper with session data to gain unauthorized access.
- **Insecure direct object references**: Accessing or modifying resources directly through references, bypassing access controls.
- **Missing access controls on API endpoints**: Failing to implement proper access controls on API endpoints, leading to unauthorized access to sensitive functionalities.
- **Privilege escalation**: Unauthorized users gaining elevated privileges, such as administrative rights, and performing actions beyond their authorized scope.
- **Metadata Manipulation**: Unauthorized modification of metadata, such as access tokens or cookies, to gain unauthorized access.
- **CORS misconfiguration**: Misconfiguring Cross-Origin Resource Sharing (CORS), allowing unauthorized access to resources from different origins.

## Mitigation Strategies

To mitigate Broken Access Control vulnerabilities, developers should implement the following strategies:

- **Implement least privilege principle**: Restrict user access to only what is necessary for their role or function within the application.
- **Centralize access control logic**: Use centralized access control mechanisms across the application to ensure consistency and reduce the risk of misconfigurations.
- **Enforce proper object-level permissions**: Ensure that users can only access and modify resources they own or are authorized to access.
- **Regularly review and update access control rules**: Continuously review and update access control rules to align with business requirements and address emerging threats.
- **Secure sensitive files and directories**: Protect sensitive files and directories from unauthorized access by implementing proper access controls and directory listing prevention measures.
- **Implement logging and monitoring**: Log access control-related events and monitor for suspicious activities, such as repeated unauthorized access attempts.
- **Enforce rate limiting**: Limit the number of requests a user can make within a certain time frame to prevent abuse and mitigate the impact of unauthorized access attempts.
- **Implement session management best practices**: Use secure session management techniques, such as expiring sessions and implementing session revocation mechanisms, to prevent unauthorized access.

## Scenario 1:

The application fails to validate user input before using it in a SQL query, allowing attackers to manipulate URLs and access unauthorized user accounts.

```
pstmt.setString(1, request.getParameter("acct"));
ResultSet results = pstmt.executeQuery();
```

```
https://example.com/app/accountInfo?acct=notmyacct
```

## Scenario 2:

The application allows regular users to access administrative pages without proper authorization, posing a security risk. Access to administrative functionalities should be restricted to authorized users only.

```
https://example.com/app/getappInfo
https://example.com/app/admin_getappInfo
```
Addressing these vulnerabilities through proper access control measures significantly enhances the security posture of web applications and protects against unauthorized access and data breaches./app/admin_getappInfo 

## Categories

- [Authorization](Authorization.md)
- [Insecure Direct Object Reference (IDOR)](Insecure_Direct_Object_Reference.md)
- [Transaction Authorization](Transaction-Authorization.md)
- [Cross-Site Request Forgery (CSRF)](Cross-Site-Request-Forgery.md)

## Let's Connect

I welcome your insights, feedback, and opportunities for collaboration. Together, we can make the digital world safer, one challenge at a time.

- **LinkedIn**: (https://www.linkedin.com/in/aashwadhaama/)

I look forward to connecting with fellow cybersecurity enthusiasts and professionals to share knowledge and work together towards a more secure digital environment.
