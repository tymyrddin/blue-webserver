# Introduction

## What?

Do not use old versions of the TLS protocol (TLSv1 TLSv1.1) on web servers, because they open the door to [SSL attacks](red-network:docs/application/ssl). 

## Why?

All the TLS versions older than 1.2 are having lots of known vulnerabilities, which is why the latest browsers have removed support for these vulnerable protocols. 

## How?

* [(Re)configure TLS](tls.md)
* [Manually specify cipher suite](cipher.md)
* [Configure forward secrecy](forward-secrecy.md)

