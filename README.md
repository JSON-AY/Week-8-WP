# Project 8 - Pentesting Live Targets

Time spent: **8** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session Hijacking: When using two seperate browsers both with BurpSuite, you can use the session id from a successfull login to then use on an alternate browser with Burp to sign in using that same users session.
[Session Hijacking](https://imgur.com/a/DbJlBl7)

Vulnerability #2: Potential for SQL Injections: When modifying the url under a salespersons name, you can see that the blue site returns a failed database query when adding a single quote after the id field. The red and green sites simple redirect back to the main salesperson page as it's been properly sanitized. 
[SQL Vulnerability](https://imgur.com/a/bQpVxAi)


## Green

Vulnerability #1: User Enumeration: When typing the name of an actual user that has access to the site, the "Log in was unsuccessful" message will be in bold, signifying that this user name exists. Whereas, if you type in a random user name the "Log in was unsuccessful" message will not be in bold text.
[User Enumeration Imgur](https://imgur.com/a/V4oltH2)

Vulnerability #2: Cross Site Scripting URL Redirect: By using the public facing feedback form, you can inject XSS attacks. I was unsuccesful in completely redirecting to the youtube site that I wanted (Rick Roll), but it shows that when a logged in user attempts to view the feedback the page tries to go where I told it to. It may not succeed in redirecting, but it does cause a headache for the web admin that they now have to fix.
[XSS URL Redirect](https://imgur.com/a/vFurN55)


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR): When loading the "Find a Salesperson" page, if you click into an employee, you'll see in the url that they are using "id" to call out specific salespeople. When changing the number, you're able to find additional salespeople that are not listed in the main directory. 
[IDOR Imgur](https://imgur.com/a/bdrdliH)

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
