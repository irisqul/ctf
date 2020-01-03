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
