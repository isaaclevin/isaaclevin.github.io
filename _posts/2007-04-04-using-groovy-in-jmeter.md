---
layout: post
title: Using Groovy in JMeter
---
*Note: This is a copy from my old blog posted in 2007. Some things mentioned here have been changed since then.*

Groovy is a great scripting language intimately integrated with Java. Being able to leverage any code written in Java and at the same time having all the advantages of dynamic programming language, makes it an excellent choice for tasks such as file management, build systems and testing.

JMeter is an open source load test tool. It supports many protocols (HTTP, FTP, JMS and others) out-of-the-box.

Many times I found myself in situation when I wanted to run load test against stand-alone Java components or against an application that uses proprietary binary TCP based protocol.
Groovy would be an excellent choice for this task. Some work on integrating JMeter and Groovy was done by [Alexandru Popescu](https://themindstorms.blogspot.com/2007/01/groovy-support-for-jmeter.html), 
however the project is not available to the public yet. Then I discovered that there is an indirect support for groovy in JMeter itself. JMeter supports BSF, which is an abstraction layer on top of many scripting languages including groovy. BSF distribution that comes with JMeter actually has some glitch in groovy support, but after upgrading to the latest version of bsf.jar it was very easy to start writing JMeter scripts in groovy.

Here the steps I followed:

download latest groovy binaries from http://groovy.codehaus.org/
copy groovy-all-1.0.jar to jmeter/lib directory
download latest bsf binaries from http://jakarta.apache.org/bsf/ (I was using version 2.4.0)
replace bsf-2.3.0.jar in jmeter/lib with bsf.jar from the version you just downloaded
start jmeter
create BSF Sampler and specify “groovy” as a scripting language (see screenshot below)
type your groovy script and run it

** Work in progress **
