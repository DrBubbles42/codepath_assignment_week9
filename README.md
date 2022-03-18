# codepath_assignment_week9
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

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: __________________

Description:

<img src="blue-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="blue-vuln2.gif">

## Green

Vulnerability #1: Username Enumeration

Description:
The Green site is vonurable to the username enumeration because a different message is sent when a valid user tries to login compared to an invalid user tries to log in. an all sites except green, when a login fails with an invalid username the same message is sent as a failed login with a valid username. On the Green site when a valid username is used the message is in bold and when there is an invalid user the message is not in bold. this can be used with a list of usernames to find what usernames are valid in a dictionary attack.

![green1](https://user-images.githubusercontent.com/25064175/158919162-c8c927b3-8a95-413c-a856-e63fd62fb6b4.gif)

Vulnerability #2: XSS

Description:
The second vulnerability for the Green site is XSS. This exploit was easy to test, a simple XSS(`<script>alert('Nick found the XSS!');</script>`) was loaded into the feadback section on each site and the green one executed the script while the others did not. 

![green2](https://user-images.githubusercontent.com/25064175/159093780-f9f1c2d3-4122-4e75-b915-8bf1a468db78.gif)

## Red

Vulnerability #1: IDOR

Description:
This vulnerability was quite simple to figure out. Each site has a section to find a salesperson. When a person is selected the url for the person contains a query parameter of id, `https://104.198.208.81/red/public/salesperson.php?id=10`. All pages have users 1-9 so an id of 10 was attempted on all sites and only the red site responded with a page that was not yet intended to be viewed.

![red1](https://user-images.githubusercontent.com/25064175/158894513-1c58c15b-3c41-4000-a1fb-a548f08f5b03.gif)

Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work


