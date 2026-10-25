# CS 305 Module Eight Journal

**Name:** Eurek Dantley Manfoumbi Ekogha
**Artifact submitted:** Artemis Financial Vulnerability Assessment Report (Project One)

---

## 1. Who was the client and what did they want?

My client was Artemis Financial, a company that makes personal financial plans for its customers. These plans cover savings, retirement, investments, and insurance. Artemis Financial wanted to update its software and make sure its web app was safe from outside attacks. My job was to look at their web app, find the security problems, and write a report with a plan to fix them.

## 2. What did I do well, and why does secure coding matter?

I did well at reading the code file by file and finding real problems. I found 11 issues, including a hardcoded database password, a database query that was not safe from SQL injection, endpoints with no login check, and an old security library. I also explained each problem in simple words and said which file it was in.

Coding securely is important because attackers look for easy mistakes. Software security protects customer data and money. For a company, it protects trust, helps avoid lawsuits and fines, and keeps the business running. One security breach can cost a company much more than it would have cost to build the software safely.

## 3. What part of the assessment was challenging or helpful?

The most helpful part was the manual code review, because it made me slow down and think like an attacker. Looking at a simple method like `deposit()` and seeing that it would accept a negative number taught me how small mistakes can become big problems. The most challenging part was the static testing step, because I had to understand the dependency-check tool and read the CVE (known vulnerability) codes for the outdated Bouncy Castle library.

## 4. How did I add layers of security, and what would I use in the future?

My plan adds several layers: logging in (authentication), checking permissions (authorization), checking user input, using safe database queries, hiding error details, and keeping libraries up to date. If one layer fails, the others still protect the app. In the future, I would use both a manual code review and automatic tools like the OWASP dependency-check plug-in. I would also pick fixes by looking at how serious each problem is. Problems like hardcoded passwords and SQL injection would be fixed first because they are the easiest for an attacker to use.

## 5. How would I make sure the code is functional and secure after changes?

In Project One, I was told to find and plan fixes, not to change the code. So my report lists the fixes but does not apply them. After making fixes in the future, I would run the app and its tests to make sure it still works. Then I would run the dependency-check scan again and review the changed code by hand to make sure I did not add new problems.

## 6. What resources, tools, or coding practices will help in the future?

- The OWASP dependency-check Maven plug-in, to find known problems in libraries
- The National Vulnerability Database and CVE codes, to learn about known security problems
- The OWASP Top 10, as a checklist of common security mistakes
- Safe coding habits: check all user input, use prepared statements, never store passwords in code, keep error messages simple, and keep libraries updated
- Eclipse and Maven for building and testing the project

## 7. What can I show future employers from this assignment?

I can show this vulnerability assessment report. It shows that I can read code, find security problems, use a scanning tool, and explain problems clearly to a client who may not be a technical person. It also shows that I can create a practical plan to fix each problem. This is useful for jobs in software development and security.
