# Week 11 - CSRF and Request Integrity

## Labs

1. **Apprentice: CSRF vulnerability with no defenses**  
   https://portswigger.net/web-security/csrf/lab-no-defenses

2. **Practitioner: CSRF where token validation depends on request method**  
   https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-validation-depends-on-request-method

3. **Practitioner: CSRF where token is not tied to user session**  
   https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-not-tied-to-user-session

4. **Practitioner: SameSite Lax bypass via method override**  
   https://portswigger.net/web-security/csrf/bypassing-samesite-restrictions/lab-samesite-lax-bypass-via-method-override

5. **Practitioner: CSRF where token validation depends on token being present**  
   https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-validation-depends-on-token-being-present

6. **Practitioner: CSRF where token is tied to non-session cookie**  
   https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-tied-to-non-session-cookie

7. **Practitioner: SameSite Strict bypass via client-side redirect**  
   https://portswigger.net/web-security/csrf/bypassing-samesite-restrictions/lab-samesite-strict-bypass-via-client-side-redirect

8. **Practitioner: CSRF with broken Referer validation**  
   https://portswigger.net/web-security/csrf/bypassing-referer-based-defenses/lab-referer-validation-broken

## Useful learning path

**Cross-site request forgery (CSRF)**:
https://portswigger.net/web-security/learning-paths/csrf

## Quick reference

A basic cross-site form:

```html
<form action="https://target.example/change-email" method="POST">
  <input type="hidden" name="email" value="test@example.net">
</form>
<script>
  document.forms[0].submit();
</script>
```

Check:
- Does the action change server-side state?
- Is authentication cookie-based?
- Is a CSRF token required?
- Is the token bound to the session?
- Is validation performed for every relevant HTTP method?
- What `SameSite` behaviour applies to the session cookie?

Common cookie attribute:

```http
Set-Cookie: session=...; Secure; HttpOnly; SameSite=Lax
```

`HttpOnly` helps against JavaScript reading a cookie.
