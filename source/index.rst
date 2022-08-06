.. Webserver mitigations documentation master file, created by
   sphinx-quickstart on Sun Jun 26 04:56:31 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Webserver mitigations
=================================================

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Apache

   docs/apache/README.md
   docs/apache/chroot-apache.md
   docs/apache/hide-info.md
   docs/apache/directory-listing.md
   docs/apache/file-system-access.md
   docs/apache/disable-ssi-exec.md
   docs/apache/mod_security.md
   docs/apache/forward-secrecy.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Nginx

   docs/nginx/README.md
   docs/nginx/chroot-nginx.md
   docs/nginx/hide-info.md
   docs/nginx/file-system-access.md
   docs/nginx/disable-ssi-exec.md
   docs/nginx/mod_security.md
   docs/nginx/forward-secrecy.md

.. toctree::
   :caption: All mitigations

   Overview <https://tymyrddin.github.io/mitigations/>
