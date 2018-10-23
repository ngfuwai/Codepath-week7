# Codepath-week7

My first exploit was from https://klikki.fi/adv/wordpress2.html. I made a comment in the front page, and I pasted a super large XSS injection into the text field. I then viewed the comment as an admin. Apparently, the visitor was able to install a backdoor according to the tutorial. 

My second exploit involved pasting <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a> into the html editor of WP. Whenever another user hovers over the link, they get an alert.

My third exploit involved the admin typing <script>alert(1)</script> as a comment in the front page. For some reason, whenever another user visits the page, the alert is executed.

My fourth exploit involved a theme download. The tutorial could be found here: https://www.mehmetince.net/low-severity-wordpress/
I edited the theme's css file, and placed an XSS script into the name argument. I then renamed the file to be the XSS script, and I zipped the folder in a disguised zipfile. When an admin downloads the zip file, the XSS script should executel. It did not work in my demo, but I still recorded my work.
