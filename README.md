# Week7
The three exploits I used were User Enumeration, Unauthenticated Stored XSS, and Authenticated Stored XSS in youtube url embeds.

1) User Enumeration:
This one is really simple, you check to see if a user exists by attempting to login with a username. Here I entered the user Admin and a random password, and the result is the site responding, saying that the password for the username Admin is incorrect. When I enter in the user jon doe and enter in a random password, the site replies, saying that the username is invalid.

2) Authenticated Stored XSS in youtube url embeds:
In this exploit, I make a new post and enter in the specific script and it would output something. This can instead be used by an attacker to load malicious code to a post. This was fixed in 4.2.13.

3) Unauthenticated Stored XSS
In this exploit, someone can reply to a post and insert script into the comment field. If the comment is large enough, in this case larger than 64kb, then what was entered will get truncated and inserted into the database. Depending on the script entered and who viewed the comment, the consequences can be major to a site. In my example I enter in just a long list consisting of 'AAAAAAA' but an attacker can use this technique to take login info or cause harm in whatever way they want. This was Fixed in 4.2.1.
