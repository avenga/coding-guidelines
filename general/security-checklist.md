# Security checklist  
- Currently used software versions contain no known vulnerabilities
- All the modules and dependencies are up to date
- Automated security and dependency checkers are in use
- No credentials, secrets or other sensitive data exposed in the repo (use git leaks or similar)
- All necessary credentials are in Passbolt(?) and are up to date
- If regular pen-test/security check is necessary, make sure it's done
- No resources are using HTTP instead of HTTPS
- No eval() is used in the code
