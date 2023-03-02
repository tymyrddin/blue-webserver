Hardening webserver
=================================================

Unlike other devices sitting behind layers of defenses and firewalls, web servers sit at the edge of the known network and are designed to share information with the outside world, the unknown. These are some notes on hardening the two most used web servers, Nginx and Apache.

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Building a sound foundation

   docs/foundation/README.md
   docs/foundation/modules.md
   docs/foundation/services.md
   docs/foundation/file-system.md
   docs/foundation/http-methods.md
   docs/foundation/users.md
   docs/foundation/mod_security.md
   docs/foundation/mod_evasive.md
   docs/foundation/logging.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Resolving TLS issues

   docs/encryption/README.md
   docs/encryption/tls.md
   docs/encryption/cipher.md
   docs/encryption/forward-secrecy.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Preventing information disclosure

   docs/disclosure/README.md
   docs/disclosure/hide-info.md
   docs/disclosure/directory-listing.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Setting HTTP security headers

   docs/http/README.md
   docs/http/check.md
   docs/http/hsts.md
   docs/http/xframe.md
   docs/http/csp.md
   docs/http/cors.md
   docs/http/permissions.md
   docs/http/referrer.md
   docs/http/xcontent.md
   docs/http/xxss.md
   docs/http/cookie.md
   docs/http/content.md
