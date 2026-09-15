# Week 5 - Cross-Site Scripting (XSS)

## Labs

1. **Apprentice: Reflected XSS into HTML context with nothing encoded**  
   https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded

2. **Apprentice: Stored XSS into HTML context with nothing encoded**  
   https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded

3. **Apprentice: DOM XSS in `document.write` sink using source `location.search`**  
   https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-document-write-sink

4. **Apprentice: DOM XSS in `innerHTML` sink using source `location.search`**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-innerhtml-sink

5. **Practitioner: Reflected DOM XSS**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-dom-xss-reflected

6. **Practitioner: Stored DOM XSS**  
   https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-dom-xss-stored

7. **Apprentice: Reflected XSS into attribute with angle brackets HTML-encoded**  
   https://portswigger.net/web-security/cross-site-scripting/contexts/lab-attribute-angle-brackets-html-encoded

8. **Apprentice: Reflected XSS into a JavaScript string with angle brackets HTML encoded**  
   https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-angle-brackets-html-encoded

## Additional learning path

**Prototype pollution** *(optional advanced JavaScript security topic)*:
https://portswigger.net/web-security/learning-paths/prototype-pollution

## Quick reference

Start with a harmless marker:

```text
xss-test-123
```

Then determine the **context** where it appears:
- HTML text;
- HTML attribute;
- JavaScript string;
- URL;
- DOM sink.

Basic test payloads:

```html
<script>alert(1)</script>
```

```html
<img src=x onerror=alert(1)>
```

HTML encoding to recognize:

```
<  ->  &lt;
>  ->  &gt;
"  ->  &quot;
'  ->  &#39;
```

For DOM XSS, trace:

```text
source -> JavaScript processing -> sink
```
