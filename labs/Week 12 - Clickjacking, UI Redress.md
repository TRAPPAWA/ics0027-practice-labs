# Week 12 - Clickjacking / UI Redress

## Labs

1. **Apprentice: Basic clickjacking with CSRF token protection**  
   https://portswigger.net/web-security/clickjacking/lab-basic-csrf-protected

2. **Apprentice: Clickjacking with form input data prefilled from a URL parameter**  
   https://portswigger.net/web-security/clickjacking/lab-prefilled-form-input

3. **Practitioner: Multistep clickjacking**  
   https://portswigger.net/web-security/clickjacking/lab-multistep

4. **Apprentice: Clickjacking with a frame buster script**  
   https://portswigger.net/web-security/clickjacking/lab-frame-buster-script

5. **Practitioner: Exploiting clickjacking vulnerability to trigger DOM-based XSS**  
   https://portswigger.net/web-security/clickjacking/lab-exploiting-to-trigger-dom-based-xss

6. **Practitioner: Exploiting XSS to bypass CSRF defenses**  
   https://portswigger.net/web-security/cross-site-scripting/exploiting/lab-perform-csrf

7. **Practitioner: DOM XSS using web messages and a JavaScript URL**  
   https://portswigger.net/web-security/dom-based/controlling-the-web-message-source/lab-dom-xss-using-web-messages-and-a-javascript-url

8. **Practitioner: SameSite Strict bypass via sibling domain**  
   https://portswigger.net/web-security/csrf/bypassing-samesite-restrictions/lab-samesite-strict-bypass-via-sibling-domain

## Useful learning path

**Clickjacking (UI redressing)**:
https://portswigger.net/web-security/learning-paths/clickjacking

## Quick reference

Basic framing concept:

```html
<iframe src="https://target.example/account"></iframe>
```

Typical overlay concept:

```css
iframe {
  position: absolute;
  opacity: 0.1;
  z-index: 2;
}
```

Defenses to recognize:

```http
X-Frame-Options: DENY
X-Frame-Options: SAMEORIGIN
Content-Security-Policy: frame-ancestors 'none'
```

Important distinction:
- CSRF tricks the browser into **sending a request**.
- Clickjacking tricks the user into **interacting with a framed interface**.
