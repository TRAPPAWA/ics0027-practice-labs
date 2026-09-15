# Week 6 - Authentication and Session Security

## Labs

1. **Apprentice: Username enumeration via different responses**  
   https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses

2. **Apprentice: 2FA simple bypass**  
   https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-simple-bypass

3. **Apprentice: Password reset broken logic**  
   https://portswigger.net/web-security/authentication/other-mechanisms/lab-password-reset-broken-logic

4. **Practitioner: Brute-forcing a stay-logged-in cookie**  
   https://portswigger.net/web-security/authentication/other-mechanisms/lab-brute-forcing-a-stay-logged-in-cookie

5. **Practitioner: Broken brute-force protection, IP block**  
   https://portswigger.net/web-security/authentication/password-based/lab-broken-bruteforce-protection-ip-block

6. **Practitioner: 2FA broken logic**  
   https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-broken-logic

7. **Practitioner: Username enumeration via response timing**  
   https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-response-timing

8. **Practitioner: Offline password cracking**  
   https://portswigger.net/web-security/authentication/other-mechanisms/lab-offline-password-cracking

## Useful learning path

**Authentication vulnerabilities**: https://portswigger.net/web-security/learning-paths/authentication-vulnerabilities

## Quick reference

Compare authentication responses by:
- HTTP status code;
- response length;
- wording;
- redirect target;
- response time;
- cookies issued.

Base64 decode:

```bash
echo 'YWRtaW46cGFzc3dvcmQ=' | base64 -d
```

Base64 encode:

```bash
printf 'admin:password' | base64
```

MD5 from the shell:

```bash
printf 'password' | md5sum
```

Useful Burp tools:
- **Repeater** for logic testing;
- **Intruder** for controlled enumeration/brute-force exercises;
- response sorting by **Length**, **Status**, or **Time**.

Authentication questions:
- Can a later step be accessed directly?
- Is the user identity taken from a request parameter?
- Is a reset token tied to the correct account?
- Is a persistent login token predictable or weakly protected?
