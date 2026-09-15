# Week 14 - Bonus Labs: API Security

There is no normal practical session. The labs are therefore completed as self-study.

## Labs

1. **Apprentice: Exploiting an API endpoint using documentation**
   https://portswigger.net/web-security/api-testing/lab-exploiting-api-endpoint-using-documentation

2. **Practitioner: Finding and exploiting an unused API endpoint**
   https://portswigger.net/web-security/api-testing/lab-exploiting-unused-api-endpoint

3. **Practitioner: Exploiting a mass assignment vulnerability**
   https://portswigger.net/web-security/api-testing/lab-exploiting-mass-assignment-vulnerability

4. **Expert: Exploiting server-side parameter pollution in a REST URL**
   https://portswigger.net/web-security/api-testing/server-side-parameter-pollution/lab-exploiting-server-side-parameter-pollution-in-rest-url

5. **Practitioner: Exploiting server-side parameter pollution in a query string**
   https://portswigger.net/web-security/api-testing/server-side-parameter-pollution/lab-exploiting-server-side-parameter-pollution-in-query-string

6. **Apprentice: Accessing private GraphQL posts**
   https://portswigger.net/web-security/graphql/lab-graphql-reading-private-posts

7. **Practitioner: Accidental exposure of private GraphQL fields**
   https://portswigger.net/web-security/graphql/lab-graphql-accidental-field-exposure

8. **Practitioner: Finding a hidden GraphQL endpoint**
   https://portswigger.net/web-security/graphql/lab-graphql-find-the-endpoint

## Useful learning paths

**API testing**: https://portswigger.net/web-security/learning-paths/api-testing

**GraphQL API vulnerabilities**: https://portswigger.net/web-security/learning-paths/graphql-api-vulnerabilities

## Quick reference

Look for:
- `/api/`;
- versioned paths such as `/api/v1/`;
- JSON request/response bodies;
- undocumented HTTP methods;
- unused endpoints;
- object properties accepted by the server but not exposed by the UI.

Useful methods:

```http
GET
POST
PUT
PATCH
DELETE
OPTIONS
```

Typical JSON:

```json
{
  "username": "student",
  "email": "student@example.net"
}
```

For mass-assignment testing, compare fields returned by the API with fields accepted on update.
