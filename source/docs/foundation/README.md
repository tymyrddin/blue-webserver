# Introduction

## What?

* Remove all unnecessary web server modules. A lot of web servers by default come with several modules that introduce security risks.
* Modify default configuration settings. 
* Install and run a web application firewall (WAF). Most web servers support the open-source ModSecurity firewall.
* If possible, either patch server software to the latest version automatically or turn on notifications for manual patching.

## Why?

Build a more secure foundation for web applications.

## How?

* [Keep only required modules](modules.md)
* [Disable unwanted services](services.md)
* [Restrict file and directory access](file-system.md)
* [Disable unwanted HTTP methods](http-methods.md)
* [Create non-root users](users.md)
* [Install and use ModSecurity](mod_security.md)
* [Install and use ModEvasive](mod_evasive.md)
* [Set up and configure logging](logging.md)
