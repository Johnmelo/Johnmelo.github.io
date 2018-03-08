---
layout: post
title: Building security test with Selenium
description: "building an anonymous bot"
modified: 2018-03-08
tags: [anonymous bot, selenium, web pentester]
---

![Smithsonian Image]({{ site.url }}/assets/img/Web-Security-Testing.jpg)
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;One day I had to build a bot to help test a web application. The purpose of this test
was basically to verify whether the voting system of the application was vulnerable or not to attacks. Telling the the results, I realized that the site was indeed vulnerable! What I liked the most about this test was the approach I used, a tool for automation (Selenium) in conjunction with Tor, yes TOR! 
</p>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The proposal was basically to cheat the voting system, simulating a possible bot contracted by some of the entities participating in the polls. As usual, I followed the manual, I tested the application as a target user of it and then went to look at the source code to find the possible points that could give voting access, and then went on to model the 'bot'.
</p>
<b>The use of Selenium.</b>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;During the test and modeling, I could see that a particular application defense mechanism, more precisely the token identifying the html element that was responsible for identifying the object voted, for some reason remained the same with each access made with the Chrome browser, soon Chrome would be in the composition of the 'attack'. The use of Selenium came about as soon as I started to simulate a target user of the application, and I would have to take some steps that would at some point be tiring, so I invoked the power of Selenium.
According to the official documentation Selenium automates the navigation, primarily idealized with the intention of testing web applications, not limited to that. Selenium has the webdriver class that provides the interaction and use of browsers such as Firefox and Chrome. For its use it is necessary to download the executables compatible with the browser to be used. Once the executables are downloaded and environment is configured, you just need to create the scripts according to your needs. The interaction with the elements of a given page is given by the WebElements class, which provides several well defined interaction methods in their respective signatures according to the documentation.
</p>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As the purpose of this post is only to make a brief report of a test performed by me, focusing primarily on the exemplification of the use of Tor in conjunction with the automator (which at least for me open a range of possibilities), I will not stick to the features of Selenium (it deserves a separate post), so I advise you to read the <a href="https://www.seleniumhq.org/docs/">official Selenium documentation</a> and <a href="http://selenium-python.readthedocs.io/">unofficial Python documentation</a>, if you have been interested in creating automated tests, it is worth reading
</p>
<b>The need for TOR.</b>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The system to be cheating had restricted votes for IP, so I would need to be changing my IP to each voting process. That way I chose to use the Tor network as a proxy. Modeling the algorithm and defined the form of interaction with the application, I started the implementation of 'bot' in Java and python. In 'pseudocode' the bot basically had this structure:
</p>
<p>
openTor();<br>
closeTor();<br>
findElement();<br>
vote();<br>
bot_process(){<br>
&nbsp;&nbsp;&nbsp;&nbsp;openTor();<br>
&nbsp;&nbsp;&nbsp;&nbsp;openChrome();<br>
&nbsp;&nbsp;&nbsp;&nbsp;findElement();<br>
&nbsp;&nbsp;&nbsp;&nbsp;vote();<br>
&nbsp;&nbsp;&nbsp;&nbsp;closeChrome();<br>
&nbsp;&nbsp;&nbsp;&nbsp;closeTor();<br>
}<br>
main(){<br>
&nbsp;&nbsp;&nbsp;&nbsp;bot_process()<br>
}<br>
</p>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I will not go through all the code I implemented here, because this bot met a specific need of my test.
However I will put the passages that I understand as generic, and in my github I will make the complete code believing that with the necessary changes it can be used in other scenarios. In my test environment I made study-level permutations between Windows 10 and Linux (Kali), so the difference in the script used in them was basically how to interact with browser processes.
</p>
<b>Excerpts in Python for Windows:</b>

![Smithsonian Image]({{ site.url }}/assets/img/example-bot)

<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The openTor() function initializes Tor. Note that at this point I do not use something specifically from Selenium, basically I use some commands pertinent to Windows, to open Tor and thus start your tunneling service. Similarly, closeTor() terminates the Tor process. I used this strategy to open the Tor Browser on Windows because I did not see another way to use Tor service without this step, since the service is linked to the Tor browser. On Linux we have the separation, so I could start and close the service faster, a script in shell or even including in the code the commands to start / close the Tor service and the BOT was running. However, this approach to open the browser in Windows was the one I used the most since the machine park in which the tests were performed was mostly composed of machines with Windows 10.
</p>
<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Finally, I encourage you to think the next time you need to test functionality and validation of your web applications, to use Selenium. Likewise if you need to test the security of your application, with several tests aimed at security requirements, as well as penetration tests that will culminate in the application exploration, use Selenium. Obvious that is not for everything, it is up to an analysis and interpretation of the pentester in knowing what to use, this is feeling. Thus, see Selenium as a powerful facilitator for the counseling of not only functional tests but also the aid of invasion tests with the creation of bots for the most varied contexts.
</p>
