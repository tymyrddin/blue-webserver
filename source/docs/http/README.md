# Introduction

## What?

Turn on additional protection for web applications. 

## Why?

Setting security headers in web applications and web server settings is an easy way to improve the resilience of your web application against many common attacks, including [cross-site scripting (XSS)](red-app:docs/techniques/xss), [clickjacking attacks](red-app:docs/techniques/clickjacking), and [information disclosure](../disclosure/README.md).

## How?

These headers can be applied globally or to a specific site in the Nginx/Apache virtual host file by adding the HTTP Security Headers to the server block.

* [Check your HTTP security headers](check.md)
* [HTTP Strict Transport Security (HSTS)](hsts.md)
* [X-Frame-Options](xframe.md)
* [Content Security Policy (CSP)](csp.md)
* [Permissions-Policy](permissions.md)
* [Referrer-Policy](referrer.md)
* [X-Content-Type-Options](xcontent.md)
* [X-XSS-Protection](xxss.md)
* [Set-Cookie](cookie.md)
* [Content-Type](content.md)

