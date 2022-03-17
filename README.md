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

Vulnerability #1: __________________

Description:

<img src="green-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="green-vuln2.gif">


## Red

Vulnerability #1: User Enumeration

Description:
This vulnerability was quite simple to figure out. Each site has a section to find a salesperson. When a person is selected the url for the person contains a query parameter of id, `https://104.198.208.81/red/public/salesperson.php?id=10`. All pages have users 1-9 so an id of 10 was attempted on all sites and only the red site responded with a page that was not yet intended to be viewed.

![red1](https://user-images.githubusercontent.com/25064175/158894513-1c58c15b-3c41-4000-a1fb-a548f08f5b03.gif)

Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work


