# Security checklist  
### How to
It's recommended to go through the checklist once per two weeks. Feel free to choose the proper period based on your project scale and life span.

### Checklist
- Currently used software versions contain no known vulnerabilities
- All the modules and dependencies are up to date
- Automated security and dependency checkers are in use
- No credentials, secrets or other sensitive data exposed in the repo, pipelines, ENV variables, wiki, etc. (use gitleaks, git-crypt, git-secrets or similar)
- If regular pen-test/security check is necessary, make sure it's done
- HTTPS is prioritized over HTTP whenever it's possible
- New risk-prone functional has been properly tested for security vulnerabilities

### More details:
To get a more detailed reference, please, follow this link - [OWASP Secure Coding Practices Quick Reference Guide](https://owasp.org/www-pdf-archive/OWASP_SCP_Quick_Reference_Guide_v2.pdf) 
