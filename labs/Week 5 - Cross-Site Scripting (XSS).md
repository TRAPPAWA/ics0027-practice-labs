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

5. **Apprentice: DOM XSS in jQuery anchor `href` attribute sink using `location.search` source**  
   https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-jquery-href-attribute-sink

6. **Apprentice: DOM XSS in jQuery selector sink using a `hashchange` event**  
   https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-jquery-selector-hash-change-event

7. **Apprentice: Reflected XSS into attribute with angle brackets HTML-encoded**  
   https://portswigger.net/web-security/cross-site-scripting/contexts/lab-attribute-angle-brackets-html-encoded

8. **Apprentice: Stored XSS into anchor `href` attribute with double quotes HTML-encoded**  
   https://portswigger.net/web-security/cross-site-scripting/contexts/lab-href-attribute-double-quotes-html-encoded

9. **Apprentice: Reflected XSS into a JavaScript string with angle brackets HTML encoded**  
   https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-angle-brackets-html-encoded

10. **Practitioner: DOM XSS in `document.write` sink using source `location.search` inside a select element**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-document-write-sink-inside-select-element

11. **Practitioner: Reflected DOM XSS**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-dom-xss-reflected

12. **Practitioner: Stored DOM XSS**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-dom-xss-stored

13. **Practitioner: Reflected XSS into a JavaScript string with single quote and backslash escaped**  
    https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-single-quote-backslash-escaped

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
