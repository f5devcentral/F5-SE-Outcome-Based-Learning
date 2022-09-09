Install software on virtual machines
====================================

**Objective**: Install the Juiceshop application with the 14.1.1 version on the two base environment virtual machines

**Why**: 

Challenges in most situations will require an application, the application chosen for the base environment is Juice Shop owned by OWASP.

Juice Shop is written in Node.js, Express and Angular. It was the first application written entirely in JavaScript listed in the OWASP VWA Directory.

The application contains a vast number of hacking challenges of varying difficulty where the user is supposed to exploit the underlying vulnerabilities. The hacking progress is tracked on a score board. Finding this score board is actually one of the (easy) challenges!

Apart from the hacker and awareness training use case, pentesting proxies or security scanners can use Juice Shop as a *guinea pig*-application to check how well their tools cope with JavaScript-heavy application frontends and REST APIs.

Translating *dump* or *useless outfit* into German yields *Saftladen* which can be reverse-translated word by word into *juice shop*. Hence the project name. That the initials *JS* match with those of *JavaScript* was purely coincidental!

Source: https://owasp.org/www-project-juice-shop/

**How**:

https://github.com/juice-shop/juice-shop 

.. note:: Version v14.1.1 