---
layout: post
title: "How the Syrian Electronic Army Hacked The Onion"
date: 2013-05-08 09:42
comments: true
categories: [security]
---
This is write-up of how the Syrian Electronic Army hacked The Onion. In summary, they phished Onion employees' Google Apps accounts via 3 seperate methods.

The SEA began by sending phishing emails to various Onion employees beginning around May 3.
{% img left /images/phish1.png 890 %}

The _Washington Post_ link actually went to a URL like
    http://hackedwordpresssite.com/theonion.php
which redirected to a URL like
    http://googlecom.comeze.com/a/theonion.com/Service.Login?&passive=1209600&cpbps=1&continue=https://mail.google.com/mail/
which asked for Google Apps credentials before redirecting to the Gmail inbox.

These emails were sent from strange, outside addresses, and they were sent to few enough employees to appear as just random noise rather than a targeted attack.
At least one Onion employee fell for this phase of the phishing attack.

Once the attackers had access to one Onion employee's account, they used that account to send the same email to more Onion staff at about 2:30 AM on Monday, May 6. Coming from a trusted address, many staff members clicked the link, but most refrained from entering their login credentials. Two staff members did enter their credentials, one of whom had access to all of our social media accounts.

After discovering that at least one account had been compromised, we sent a company-wide email to change email passwords immediately. The attacker used their access to a different, undiscovered compromised account to send a duplicate email which included a link to the phishing page disguised as a password-reset link. This dupe email was not sent to any member of the tech or IT teams, so it went undetected. This third and final phishing attack compromised at least 2 more accounts. One of these accounts was used to continue owning our Twitter account.

At this point the editorial staff began publishing articles inspired by the attack. The second article, [Syrian Electronic Army Has A Little Fun Before Inevitable Upcoming Deaths At Hands Of Rebels](http://www.theonion.com/articles/syrian-electronic-army-has-a-little-fun-before-ine,32324/), angered the attacker who then began posting editorial emails on their Twitter account. Once we discovered this, we decided that we could not know for sure which accounts had been compromised and forced a password reset on every staff member's Google Apps account.

In total, the attacker compromised at least 5 accounts. The attacker logged in to compromised accounts from 46.17.103.125 which is also where the SEA [hosts a website](http://46.17.103.125/en/site/index).

# Don't let this happen to you

From examining the details of this incident, as well as those effecting the AP, Guardian and others, it's clear that the SEA is not using complex methods of attack. All of the hacks so far have been a result of simple phishing, or possibly dictionary attacks—all of which are preventable with a few simple security measures.

* Make sure that your users are educated, and that they are suspicious of all links that ask them to log in, regardless of the sender.

* The email addresses for your twitter accounts should be on a system that is isolated from your organization's normal email. This will make your Twitter accounts virtually invulnerable to phishing (providing that you're using unique, strong passwords for every account).

* All twitter activity should go through an app of some kind, such as HootSuite. Restricting password-based access to your accounts prevents a hacker from taking total ownership, which takes much longer to rectify.

* If possible, have a way to reach out to all of your users outside of their organizational email. In the case of the Guardian hack, the SEA posted screenshots of multiple internal security emails, probably from a compromised email address that was overlooked.

