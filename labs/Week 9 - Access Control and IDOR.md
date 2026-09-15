# Week 9 - Access Control and IDOR

## Labs

1. **Apprentice: Unprotected admin functionality**  
   https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality

2. **Apprentice: User role controlled by request parameter**  
   https://portswigger.net/web-security/access-control/lab-user-role-controlled-by-request-parameter

3. **Apprentice: Insecure direct object references**  
   https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references

4. **Practitioner: Method-based access control can be circumvented**  
   https://portswigger.net/web-security/access-control/lab-method-based-access-control-can-be-circumvented

5. **Apprentice: User role can be modified in user profile**  
   https://portswigger.net/web-security/access-control/lab-user-role-can-be-modified-in-user-profile

6. **Apprentice: User ID controlled by request parameter with data leakage in redirect**  
   https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter-with-data-leakage-in-redirect

7. **Practitioner: URL-based access control can be circumvented**  
   https://portswigger.net/web-security/access-control/lab-url-based-access-control-can-be-circumvented

8. **Practitioner: Multi-step process with no access control on one step**  
   https://portswigger.net/web-security/access-control/lab-multi-step-process-with-no-access-control-on-one-step

## Quick reference

Test access control by changing:
- object IDs;
- usernames;
- account IDs;
- roles;
- HTTP methods;
- URL paths.

Example:

```http
GET /account?id=123 HTTP/1.1
```

Try to reason about:

```text
123 -> 124
your username -> another username
GET -> POST
POST -> GET
normal endpoint -> administrative endpoint
```

Three useful categories:
- **Vertical access control:** ordinary user reaches administrator functionality.
- **Horizontal access control:** one user reaches another user's resources.
- **Context-dependent access control:** access is allowed only in an expected workflow/state.
