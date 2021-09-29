# Default web server index

A bit better default index page for web servers. Comes with some images and basic styling.

And example NGINX config fragment:

``` nginx
root /var/www/host.dev;

index index.html;

error_page 401 /401.html;
error_page 403 /403.html;
error_page 404 /404.html;
```
