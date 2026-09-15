# Week 13 - Bonus Labs: Information Disclosure, Caching, and Software Analysis

There is no normal practical session. The labs are therefore completed as self-study.

## Labs

1. **Apprentice: Source code disclosure via backup files**  
   https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-via-backup-files

2. **Practitioner: Information disclosure in version control history**  
   https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-in-version-control-history

3. **Apprentice: Exploiting path mapping for web cache deception**  
   https://portswigger.net/web-security/web-cache-deception/lab-wcd-exploiting-path-mapping

4. **Practitioner: Web cache poisoning with an unkeyed header**  
   https://portswigger.net/web-security/web-cache-poisoning/exploiting-design-flaws/lab-web-cache-poisoning-with-an-unkeyed-header

5. **Apprentice: Information disclosure on debug page**  
   https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-on-debug-page

6. **Apprentice: Information disclosure in error messages**  
   https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-in-error-messages

7. **Practitioner: Web cache poisoning with an unkeyed cookie**  
   https://portswigger.net/web-security/web-cache-poisoning/exploiting-design-flaws/lab-web-cache-poisoning-with-an-unkeyed-cookie

8. **Practitioner: Exploiting path delimiters for web cache deception**  
   https://portswigger.net/web-security/web-cache-deception/lab-wcd-exploiting-path-delimiters

## Useful learning path

**Web cache deception**:
https://portswigger.net/web-security/learning-paths/web-cache-deception

## Quick reference

Files and locations worth recognizing during authorized source/structure analysis:

```text
.git/
.git/HEAD
.git/config
.bak
.old
~
robots.txt
```

Useful Git commands when a repository is legitimately available for analysis:

```bash
git log --oneline --all
git show <commit>
git diff <commit1> <commit2>
```

Cache-related headers may include:

```http
Cache-Control:
Age:
Vary:
X-Cache:
```

Ask two separate questions:
1. How does the **origin server** interpret this path/request?
2. How does the **cache/CDN** interpret it?

If their answers differ, interesting things start happening.