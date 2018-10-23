# Codepath-week7

My first exploit was from https://klikki.fi/adv/wordpress2.html. I made a comment in the front page, and I pasted a super large XSS injection into the text field. I then viewed the comment as an admin. Apparently, the visitor was able to install a backdoor according to the tutorial. The versions of WP affected are WordPress <= 4.2  and the exploit is Unauthenticated Stored Cross-Site Scripting (XSS)

My second exploit involved pasting <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a> into the html editor of WP. Whenever another user hovers over the link, they get an alert. The versions affected are WP <=4.2 and the vulnerability is Authenticated Stored Cross-Site Scripting (XSS)

My third exploit involved the admin typing <script>alert(1)</script> as a comment in the front page. For some reason, whenever another user visits the page, the alert is executed. This exploit is improvised, and I did not find a tutorial for this exploit. Therefore, I am not clear on what this vulnerability is called.

My fourth exploit involved a theme download. The tutorial could be found here: https://www.mehmetince.net/low-severity-wordpress/
I edited the theme's css file, and placed an XSS script into the name argument. I then renamed the file to be the XSS script, and I zipped the folder in a disguised zipfile. When an admin downloads the zip file, the XSS script should executel. It did not work in my demo, but I still recorded my work. The versions of WP affected are WordPress 3.4-4.7 and the vulnerability is called Stored Cross-Site Scripting (XSS) via Theme Name fallback
