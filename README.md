# everlasting-botstopper
Stop spammers with your Lighttpd config!


## About
 These are some configuration rules for Lighttpd that block common spam crawlers and search engines that don't 
 honor robots.txt. I use this over at http://www.ctis.me to block annoying bots and such that I constantly see in my webserver access
 logs, and it works extremely well.

 By default blocked requests are logged to the file /var/log/lighttpd/spam.log, but this can be changed to whatever you like. 

 Blocking spam crawlers is important because it will help make sure that personal information that may be on your site, such as phone
 numbers or emails, don't get picked up by spammers. It also keeps your webserver from serving web pages to robots who often make many
 requests at a time, thus freeing bandwidth and system resources for legitimate visitors.

 Check out http://blog.ctis.me/2015/05/blocking-bad-bots-in-3-easy-steps-in.html for some more information.

## Installation
 Installation is simple, simply paste this into a file named spam.conf in /etc/lighttpd/, then,  in your lighttpd configuration, add the line: 

    include /etc/lighttpd/spam.conf

 Once finished, run the command:
    
    sudo /etc/init.d/lighttpd reload && sudo /etc/init.d/lighttpd restart

 Or, you could copy and paste this into your /etc/lighttpd/lighttpd.conf, and run the above command.
 For other webservers, these regular expressions should carry over, but I can't guarantee it. 
 If in doubt, consult your documentation.

## Suggestions and reporting

 If you have any suggestions for new rules that should be added, or perhaps have questions or concerns, 
 please leave a comment or send an email to ct[ at] charltontrezevant.com. I'd love to hear from you!
