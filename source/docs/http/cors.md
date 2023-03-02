# Cross-Origin Resource Sharing (CORS)

The `Access-Control-Allow-Origin` response header indicates whether the response can be shared with requesting code from the given origin.

Web browsers enforce the same-origin policy, which restricts resource sharing across different origins. Cross-origin resource sharing, or CORS, is the mechanism through which we can overcome this barrier. 

Websites often loosen the same-origin policy (SOP) to have more flexibility with CORS. These controlled and intended SOP bypasses can have adverse effects, as attackers can sometimes [exploit misconfigurations in these techniques](red-app:docs/techniques/sop). These exploits can cause private information leaks and lead to more vulnerabilities, such as authentication bypass, account takeover, and large data breaches.

## Nginx

A shot (needs a lot more work, and testing):

```text
set $cors '';
    # Extend the list of XSS-whitelisted domains by adding more
    if ($http_origin ~ '^http[s]*?://(foo\.bar|.+\.foo\.bar|fou\.baar|.+\.fou\.baar)') {
        set $cors T;
    }

    if ($request_method = 'OPTIONS') {
        set $cors "${cors}O";
    }

    if ($cors = 'T') {
        add_header 'Access-Control-Allow-Origin' "$http_origin" always;
        add_header 'Access-Control-Allow-Credentials' 'true' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, DELETE, OPTIONS' always;
        add_header 'Access-Control-Allow-Headers' 'Accept,Authorization,Cache-Control,Content-Type,DNT,If-Modified-Since,Keep-Alive,Origin,User-Agent,X-Requested-With' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,X-Mx-ReqToken,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type';

        #add_header 'Access-Control-Expose-Headers' 'Authorization' always;
    }

    if ($cors = 'O') {
        add_header 'Access-Control-Max-Age' 1728000;
        add_header 'Content-Type' 'text/plain charset=UTF-8';
        add_header 'Content-Length' 0;
        return 204;
    }

    if ($cors = 'TO') {
        add_header 'Access-Control-Allow-Origin' "$http_origin" always;
        add_header 'Access-Control-Allow-Credentials' 'true' always;
        add_header 'Access-Control-Allow-Methods' 'GET, POST, PUT, DELETE, OPTIONS' always;
        add_header 'Access-Control-Allow-Headers' 'Accept,Authorization,Cache-Control,Content-Type,DNT,If-Modified-Since,Keep-Alive,Origin,User-Agent,X-Requested-With' always;
        add_header 'Access-Control-Allow-Headers' 'DNT,X-Mx-ReqToken,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type';

        add_header 'Access-Control-Max-Age' 1728000;
        add_header 'Content-Type' 'text/plain charset=UTF-8';
        add_header 'Content-Length' 0;
        return 204;
    }
```

## Resources

* [MDN Web docs: Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
* [MDN Web docs: Access-Control-Allow-Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin)
* [CORS on Nginx](https://enable-cors.org/server_nginx.html), but uses `*`
* [Nginx Access-Control-Allow-Origin and CORS](https://distinctplace.com/2017/04/17/nginx-access-control-allow-origin-cors/)
* [How to Set Access-Control-Allow-Origin (CORS) Headers in Apache](https://ubiq.co/tech-blog/set-access-control-allow-origin-cors-headers-apache/)