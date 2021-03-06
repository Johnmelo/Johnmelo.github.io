---
layout: post
title: Software Security, be prepared.
description: "First article about software security, what is? and contextualization"
modified: 2018-03-02
tags: [software security]
---

![Smithsonian Image]({{ site.url }}/assets/img/hacking.jpg)

<p>
A few months ago I started writing a pre-project with the intention of submitting it to the master's degree in systems and computing offered by UFRN. On the first attempt it did not have success, the text contained some flaws and I did not have time to correct until the maximum deadline for submission, however after re-reading several times and make the corrections, I thought that will be interesting start my blog posts here by writing about the central theme of this work, which, as we see it day after day, there is a huge need not only for new professionals, but also for professionals who already work in development with medium knowledge (at least) in the concept of software security. 
</p>

<p>
<b>What is software security?</b>
</p>

<p>
Software security studies and plans how a particular software behaves if it is the target of some kind of attack. Security will always be tied to the information and services being protected, so that software security must be thought throughout the software life cycle, meeting the security requirements raised for the construction of the same.
</p>

<p>
<b>Okay Jonathas, but what's the need?</b>
</p>

<p>
If we look at the latest threats and exploits to computer systems, we see that, all IT peoples staing stunned, raising their firewalls, IDS and IPS, running to upgrade their software with the famous patches (this is not wrong, it is a praiseworthy and correct attitude), however we forget that many times that exploration could only be performed due to a failure in a software (OS, libraries, APIs, SOFTWARES) internal to the system. Schneier wrote "we should not have to spend a lot of time, money and effort on network security if we did not have such poor software security." And this is still true! According to our needs and services provided, we have chosen and installed software that helps make our services available and / or offered. It may be that in this process is used a certain third party software, consolidated in the market, "properly tested", but what do we do if this software has some vulnerability that will culminate in a exploitation? Will our firewall stop it? Will our IDS detect the attack? Will our IPS make you suffer in the hand of the hacker? Those are valid questions, difficult to give a 100% response to one side, because we would have to explain, and thus know, what kind of vulnerability we are being exposed. However, these issues make me realize that once I create a vulnerable software, not only the software itself is susceptible to exploitation and data leakage, but the systems on which it was deployed also has the risk of an attacker across that vulnrability to steal data and perform the most diverse atrocities contained in your mind.
</p>

<p>
So application developers, do you have ideas or strategies that will help you defend your software? I tell you it must be more than a defensive programming. xD

Here are some key points that should be part of your ways of developing, especially if your software works with critical data (but not only that, remember that even if your software is a note application, if it is vulnerable, the systems that it is installed will run a certain risk of being violated through of your software). Are they:
</p>

1. <b>Understand the main vectors of software security threats</b> (I'll explain in another post). Something like buffer overflow, injection, reversing etc, must be known by who develop, once we know we can have good ideas about how we will design an application more resistant to these threats.
2. <b>Develop security requirements.</b> Once you know the main sources of threats and understand security issues relevant to your application domain, security requirements can be lifted, modeled and ready to be serviced!
3. <b>Invest in the test of your application.</b> Come on, you will see only benefit by developing and running good tests on your application. Give value to deliver secure software for your customers, realize that software security goes hand in hand with its quality. (we will have a post driven to Software Test, with more details)
4. <b>Think about security throughout the development process of your application</b>. I mean that this point is our recursion, covering the software life cycle.

<p>
To finish I leave some tips from books that approach infinitely better than I, the core concept of this post.
</P>

* The Art of Software Security Assessment: Identifying and Preventing Software Vulnerabilities (DOWD, Mark; MCDONALD, John; SCHUH, Justin.)
* Building Secure Software: How to Avoid Security Problems the Right Way (VIEGA, John; MCGRAW, Gary)
* Cyber Security Engineering: A Practical Approach for Systems and Software Assurance (MEAD, Nancy R.; WOODY, Carol C.)
* Writing Secure Code (MICHAEL HOWARD, DAVID LEBLANC)
* How to Break Software: A Practical Guide to Testing (Whittaker, James A.)

<p>
Super I recommend 'Writing Secure Code' book, it is what I am currently reading.
See you!
<p/>

