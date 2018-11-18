# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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

Vulnerability #1: __________________

Vulnerability #2: __________________


## Green

Vulnerability #1: User Enumeration: When typing the name of an actual user that has access to the site, the "Log in was unsuccessful" message will be in bold, signifying that this user name exists. Whereas, if you type in a random user name the "Log in was unsuccessful" message will not be in bold text.
[User Enumeration] (https://imgur.com/a/V4oltH2)

Vulnerability #2: __________________


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR): When loading the "Find a Salesperson" page, if you click into an employee, you'll see in the url that they are using "id" to call out specific salespeople. When changing the number, you're able to find additional salespeople that are not listed in the main directory. 
[IDOR](https://imgur.com/a/bdrdliH)

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
