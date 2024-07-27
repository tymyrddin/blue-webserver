# Introduction

## What?

You can send GET and POST requests cross domain even if a target does not use CORS, but there are restrictions. Most importantly, the response can not be read. This restriction is built into browsers as part of the [Single Origin Policy (SOP)](https://webapp.tymyrddin.dev/docs/techniques/sop) and it protects against data leaking across domains. It also stops publishing an API that can be read from other domains.

## Why?

CORS allows for loosening that restriction, allowing the domain that is hosting the API to announce to browsers that it allows cross domain calls from either all or some defined domains. 

If misconfigured, these controlled and intended SOP bypasses can have adverse effects. Such exploits can cause private information leaks and lead to more vulnerabilities, such as authentication bypass, account takeover, and large data breaches.

Proper configuration of CORS is therefor essential.

## How?

* [CORS best practices](requirements.md)
* [CORS on Nginx](nginx.md)
* [CORS on Apache](apache.md)