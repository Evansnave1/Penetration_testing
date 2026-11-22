# Penetration Testing Portfolio

## Bug Bounty Lab — DVWA on Metasploitable2

This project documents a security assessment of Damn Vulnerable Web Application (DVWA) in a controlled Metasploitable2 lab. The assessment covered service discovery, authentication, database input handling, file upload controls, and host privilege boundaries.

| Finding | Security impact | Remediation |
| --- | --- | --- |
| Weak login protections | Repeated password guesses can lead to account takeover. | Rate-limit attempts, monitor failed logins, and require multi-factor authentication where practical. |
| SQL injection | Untrusted input can change a query and expose data that the application should protect. | Use parameterized queries and restrict database account permissions. |
| Unsafe file uploads | The web server can execute uploaded content if uploads are stored in an executable location. | Allowlist file types, validate contents, and store uploads outside the web root. |
| Host privilege escalation | A compromised application can lead to broader host compromise when privilege boundaries fail. | Patch the host, run services with least privilege, and audit privileged executables and services. |
