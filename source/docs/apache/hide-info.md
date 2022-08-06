# Hide version and OS identity

Open up `/etc/apache2/conf.d/security` and set:

    ServerTokens Prod
    ServerSignature Off

And restart Apache web server. 

## Related attack trees

* [Reconnaissance](attack-trees:docs/reconnaissance/README)

