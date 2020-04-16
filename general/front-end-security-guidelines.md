### HTTPS
Make sure all of your resources are being loaded through a secured HTTPS connection and all client-server communication is happening through an HTTPS protocol. Also, keep an eye out for an unsecured connections initiated by a third-party dependencies.

### User input validation and escaping to prevent XSS
Data that is being provided by the user should always be strictly validated and escaped before sent to the server. Make sure there are no possible scenarios for XSS through user generated data. To prevent this kind of vulnerabilities measures should be taken both at the server side and on the client.

### Using untrusted data in the DOM (DomXSS)
Any time you need to insert some data directly to the DOM, make sure to do it in the right way. 
If you’re using data from the server (especially 3rd-party), it should not be received as an HTML ready to be inserted to the DOM straight away. The preferred way is to send the data in JSON format, parse and validate it on the client side and then use the data as required.
If you have to put some data provided by the user in the DOM, make sure it’s properly validated and sanitised (doesn’t contain any HTML, styles or scripts in it) before using it. Some modern frameworks will do that for you but not all of them, so keep that in mind. 
Every time you have to use dangerouslySetInnerHTML in your frontend framework, dynamically place user input into a.href, style or other HTML attributes that support “javascript:” option, think twice and try to avoid doing that. If it's unavoidable, prefer using [createTextNode](https://developer.mozilla.org/en-US/docs/Web/API/Document/createTextNode) if possible.

### Avoid eval()
Not only is code using eval() is highly prone to error and a serious performance hit, but it’s also a dangerous security vulnerability. There’s very little chance you really need to use eval() to make your code work as desired, so, please, avoid it.

### Broken authentication
There’s a number of things that could go wrong with your authentication flow. Let’s go through the most common scenarios.
#### Putting Session ID in the URL (ex: http://example.com/&sessionid=3FAN8DKFNVMDPOSLAFK7R)
This exposes the session identifier, furthermore, if the user shares the link with somebody they’ll use his session. Luckily this is a pretty old technique and almost nobody does it nowadays, but you have to be aware of it just in case.
Also, it's recommended to avoid sending any sensitive data in GET-Parameters because of number of reasons: they will create a log entry within the server like `XXX - - [09/Apr/2020:14:11:04 +0200] "GET /login.php?username=test&password=secret HTTP/1.1" 200 55875 "https://example.com/login.php?username=test&password=secred" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:62.0) Gecko/20100101 Firefox/62.0"`, will be stored in browser history (therefore exposed), etc. 
#### Session expiration (session id / token expiration)
No session time out, or a very long expiration time means that if the user doesn’t intentionally choose to log out, his session maybe used by other people from the same browser in any moment of time. Also, if attacker managed to get user’s session id or token, he’ll be able to use it indefinitely.

### Sensitive data on the client
Never store any sensitive data (login credentials, user’s personal info, etc) on the client side unless it’s really necessary. If you do need it, make sure it’s well protected, deleted as soon as possible and is only received and stored in the amount limited by the requirements without any excessive/unneeded fields and attributes.

### Sensitive data in the repository
No sensitive data, such as hardcoded login credentials, tokens, secrets, private URLs, etc, should make its way into the VCS repository. If there’s no other way except for using hardcoded sensitive data, make sure it’s stored in a separate file which is listed in the .gitignore (or equivalent) or protected/encrypted (ex: [git-crypt](https://github.com/AGWA/git-crypt)) in any suitable way.

### No hidden inputs with valuable data
Don’t use any "hidden input” approaches for valuable data, because they can be easily exploited

### Update dependencies
Make sure your dependencies are up to date and no known vulnerabilities exist. If you’re using npm, pay attention to its audit output and take actions required.

### More information
Please, visit https://owasp.org/www-project-top-ten/ for the most often found vulnerabilities within web projects.
