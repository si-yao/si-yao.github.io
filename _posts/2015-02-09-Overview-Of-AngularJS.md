---
layout: post
title: "Overview of Angular JS"
description: "Custom written post descriptions are the way to go... if you're not lazy."
tags: [technology]
image:
  feature: abstract-3.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: true
share: true
---

#AngularJS?

<img src="https://angularjs.org/img/AngularJS-large.png">

Based on JavaScript, like PHP and other script languages, can do (virtually) everything at client side. 

#Build Website by AngularJS?
It is enough! 

##How to deploy on server?

I was confused by this. Because you can click the html file and see the website, but how to access via Internet? Apache server! It holds files on server, very powerful!

##Sometimes need more

###Bower?
Package denpendecy manager. Declare lib dependency in bower.json, and type "bower install" to download all js libs. It is like maven in Java, but more light-weighted.

###Grunt?
Make script alive. It is "task runner", doing automations. Simply, it is something outside AngularJS, and do testing, minimize js libs into 1 file, and also can start up a server for scripts. Then you don't need Apache server any more.

#Enough by AngularJS?
Not really! Script is mainly used for loading views and handling some logic by controller in the middle. But cannot take heavy tasks. So we need more! MEAN.JS is a solution! MongoDB, Express, AngularJS, NodeJS. We have focused on AngularJS on client side. Now, M+E+N build the back-end server. Express is the web framework building on NodeJS, making it easier to handle web events. And NodeJS is server-side JS which connects MongoDB. MongoDB creates/ updates/ inserts/ deletes/ queries Json-format data. 

#General View of App
Generally, back-end server runs REST service. And front-end AngularJS makes request to REST server, and gets data to update views. That is very similar to mobile App dev. Client side code is equivalent to mobile app code, which both make request to REST server (or other ways) to obtain required data to update views. But mobile app is more complicated as it has cache mechanism so that can run offline as well. 

Some traditional web apps, according to my understanding, are more rigid for front/back-end binding. Like structs in J2EE, the web app runs on the web container, and catch URL request, then route it to some functions to do logics, and then render the view page (asp for example), injecting data and loading the view. The workflow is like: request ->(struts) back-end -> view with data. And the web work with REST service is like: request -> view without data(js/php) -> back-end(restful) -> view with data.

#Conclusion
Should learn more!	