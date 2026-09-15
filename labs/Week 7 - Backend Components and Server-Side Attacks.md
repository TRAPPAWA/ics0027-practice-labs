# Week 7 - Backend Components and Server-Side Attacks

## Labs

1. **Apprentice: File path traversal, simple case**  
   https://portswigger.net/web-security/file-path-traversal/lab-simple

2. **Practitioner: File path traversal, traversal sequences stripped non-recursively**  
   https://portswigger.net/web-security/file-path-traversal/lab-sequences-stripped-non-recursively

3. **Practitioner: File path traversal, validation of file extension with null byte bypass**  
   https://portswigger.net/web-security/file-path-traversal/lab-validate-file-extension-null-byte-bypass

4. **Apprentice: OS command injection, simple case**  
   https://portswigger.net/web-security/os-command-injection/lab-simple

5. **Practitioner: Blind OS command injection with time delays**  
   https://portswigger.net/web-security/os-command-injection/lab-blind-time-delays

6. **Apprentice: Remote code execution via web shell upload**  
   https://portswigger.net/web-security/file-upload/lab-file-upload-remote-code-execution-via-web-shell-upload

7. **Apprentice: Web shell upload via Content-Type restriction bypass**  
   https://portswigger.net/web-security/file-upload/lab-file-upload-web-shell-upload-via-content-type-restriction-bypass

8. **Apprentice: Basic SSRF against the local server**  
   https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-localhost

9. **Practitioner: File path traversal, traversal sequences stripped with superfluous URL-decode**  
   https://portswigger.net/web-security/file-path-traversal/lab-superfluous-url-decode

10. **Apprentice: Basic SSRF against another back-end system**  
    https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-backend-system

## Useful learning paths

**Server-side vulnerabilities**:
https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice

**Path traversal**:
https://portswigger.net/web-security/learning-paths/path-traversal

**File upload vulnerabilities**:
https://portswigger.net/web-security/learning-paths/file-upload-vulnerabilities

**Server-side request forgery (SSRF) attacks**:
https://portswigger.net/web-security/learning-paths/ssrf-attacks

## Quick reference

Path traversal patterns:

```text
../
../../
../../../etc/passwd
..\..\..\windows\win.ini
```

Common encoded variants:

```text
..%2f
%2e%2e%2f
..%252f
```

Null byte notation:

```text
%00
```

Common command separators on Unix-like systems:

```text
;
&&
||
|
```

Simple timing probe:

```text
sleep 5
```

Useful upload checks:
- filename extension;
- MIME / `Content-Type`;
- actual file contents;
- where uploaded files are served;
- whether the server executes uploaded content.

SSRF targets often worth understanding inside the Academy environment:

```text
http://127.0.0.1/
http://localhost/
```
