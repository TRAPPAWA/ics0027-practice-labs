# Week 4 - Client-Side Controls and DOM Behaviour

## Labs

1. **Apprentice: Excessive trust in client-side controls**  
   https://portswigger.net/web-security/logic-flaws/examples/lab-logic-flaws-excessive-trust-in-client-side-controls

2. **Practitioner: DOM-based open redirection**  
   https://portswigger.net/web-security/dom-based/open-redirection/lab-dom-open-redirection

3. **Practitioner: DOM-based cookie manipulation**  
   https://portswigger.net/web-security/dom-based/cookie-manipulation/lab-dom-cookie-manipulation

4. **Apprentice: High-level logic vulnerability**  
   https://portswigger.net/web-security/logic-flaws/examples/lab-logic-flaws-high-level

5. **Apprentice: Inconsistent security controls**  
   https://portswigger.net/web-security/logic-flaws/examples/lab-logic-flaws-inconsistent-security-controls

6. **Apprentice: Flawed enforcement of business rules**  
   https://portswigger.net/web-security/logic-flaws/examples/lab-logic-flaws-flawed-enforcement-of-business-rules

7. **Practitioner: DOM XSS using web messages**  
   https://portswigger.net/web-security/dom-based/controlling-the-web-message-source/lab-dom-xss-using-web-messages

8. **Practitioner: DOM XSS using web messages and `JSON.parse`**  
   https://portswigger.net/web-security/dom-based/controlling-the-web-message-source/lab-dom-xss-using-web-messages-and-json-parse

## Quick reference

Client-side controls are **not security boundaries**.

Things to try:
- change disabled or hidden form values before sending the request;
- modify prices, IDs, roles, quantities, or workflow parameters in Burp;
- send requests directly from Repeater without using the browser UI;
- inspect JavaScript for sources and sinks.

Common DOM sources:

```javascript
location
location.search
location.hash
document.URL
document.cookie
```

Common sinks:

```javascript
location = value
location.href = value
document.write(value)
element.innerHTML = value
```

URL decoding from a shell:

```bash
python3 -c "import urllib.parse; print(urllib.parse.unquote('%2Fadmin%3Fid%3D1'))"
```

URL encoding:

```bash
python3 -c "import urllib.parse; print(urllib.parse.quote('../admin?id=1'))"
```