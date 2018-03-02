---
layout: post
title: Software Security, be prepared.
description: "First article about software security, what is? and contextualization"
modified: 2018-03-02
tags: [software security]
---

![Smithsonian Image]({{ site.url }}/assets/img/hacking.jpg)

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A few months ago I started writing a pre-project with the intention of submitting it, and thus succeeding, in the master's degree in systems and computing offered by UFRN. On the first attempt it did not work, the text contained some flaws and I did not have time to correct until the maximum deadline for submission, however after re-reading several times and make the corrections due, I managed to pass. Although I am not working with my pre project as a de facto project in the master's degree, I will not expose the same since I have some pretensions for it. However, I want to start my blog posts here by writing about the central theme, which, as we see it day after day, there is a huge need not only for new professionals, but also for professionals who already work in development with medium knowledge (at least) in the concept of software security.
</p>

<p>
<b>What is software security?</b>
</p>

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Software security studies and plans how a particular software behaves if it is the target of some kind of attack. Security will always be tied to the information and services being protected, so that software security must be thought throughout the software life cycle, meeting the security requirements raised for the construction of the same.
</p>

<p>
<b>Okay Jonathas, but what's the need?</b>
</p>

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If we look at the latest threats and exploits by hackers to computer systems, we see that, of course, all IT people are already stunned, raising their firewalls, IDS and IPS, running to upgrade their software with the famous patches (this is not wrong, it is a praiseworthy and correct attitude), however we forget that many times that exploration could only be performed due to a failure in a software (OS, libraries, APIs, SOFTWARES) internal to the system. A phrase that sums it up is what Schneier wrote "we should not have to spend a lot of time, money and effort on network security if we did not have such poor software security." And this is still true! According to our needs and services provided, we have chosen and installed software that helps make our services available and / or offered. It may be that in this process is used a certain third party software, consolidated in the market, "properly tested", but what if this software has some vulnerability that will culminate in a exploitation? Your firewall will stop? Will your IDS detect the attack? Will your IPS make you suffer in the hand of the hacker? They are valid questions, difficult to give a 100% response to one side, because we would have to explain, and thus know, what kind of vulnerability we are being exposed. However, these issues make me realize that once I own a vulnerable software, not only the software itself is susceptible to exploitation and data leakage, but the systems on which it was deployed also run the risk of an attacker finding it a loophole to steal data and perform the most diverse atrocities contained in your mind.
</p>

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;So application developers, do you have ideas for strategies that will help you defend your software? I tell you it must be more than a defensive programming. xD

Here are some key points that should be part of your ways of developing, especially if your software works with critical data (but not only that, remember that even if your software is a note application, if it is vulnerable, the systems that it is installed will run a certain risk of being violated through its software). Are they:
</p>

1. <b>Understand the main vectors of software security threats</b> (I'll explain in another post). Something like buffer overflow, injection, reversing etc, must be known by those who develop, once we know we can have good ideas on how we will design an application more resistant to these threats.
2. <b>Develop security requirements.</b> Once you know the main sources of threats and understand security issues relevant to your application domain, security requirements can be lifted, modeled and ready to be serviced!
3. <b>Invest in the test of your application.</b> Come on, you will only benefit by developing and running good tests on your application. Preze to deliver secure software for your customers, realize that software security goes hand in hand with its quality. (we will have a post driven to Software Test, with more details)
4. <b>Think about security throughout the development process of your application</b>. I think this point is our recursion, covering the software life cycle.

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To finish I leave some tips from books that approach infinitely better than I, the core concept of this post.
</P>

* The Art of Software Security Assessment: Identifying and Preventing Software Vulnerabilities (DOWD, Mark; MCDONALD, John; SCHUH, Justin.)
* Building Secure Software: How to Avoid Security Problems the Right Way (VIEGA, John; MCGRAW, Gary)
* Cyber Security Engineering: A Practical Approach for Systems and Software Assurance (MEAD, Nancy R.; WOODY, Carol C.)
* Writing Secure Code (MICHAEL HOWARD, DAVID LEBLANC)

<p>
Super I recommend 'Writing Secure Code' book, it is what I am currently reading.
See you!
<p/>

