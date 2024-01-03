# Default web server index

A bit better default index page for web servers. Comes with some images and basic styling.

## Example

Deployment:

``` sh
$ cd /var/www
$ sudo git clone https://github.com/retifrav/default-web-server-index.git some
$ sudo chown -R www-data:www-data ./some
```

NGINX config:

``` nginx
server {
    listen 80;
    server_name localhost;
    
    location / {
        root /var/www/some;
        index index.html;
    }

    error_page 404 /404.html;
    error_page 403 /403.html;
    error_page 401 /401.html;
}
```
