# nginx-autoindex-theme
A simple theme for nginx for autoindexed directories

<img src="https://raw.githubusercontent.com/somik123/nginx-autoindex-theme/main/screenshot.png" />

.

## How to use

Create a directory called `theme` under your nginx web root directory.

If you are using the nginx default directory, it is `/var/www/html` so the theme directory will be located in `/var/www/html/theme`

Add indexing to your root directory:
```
        location / {
                autoindex              on;
                autoindex_exact_size   off;
                autoindex_localtime    on;
                add_before_body        "/theme/nginx-before.html";
                add_after_body         "/theme/nginx-after.html";

                # Other codes goes here....
                # ......
                # ......
        }
```

If you want to add autoindex to your sub directory:

```
        location /public {
                autoindex              on;
                autoindex_exact_size   off;
                autoindex_localtime    on;
                add_before_body        "/theme/nginx-before.html";
                add_after_body         "/theme/nginx-after.html";

                # Other codes goes here....
                # ......
                # ......
        }
```
> **Note:** The `/theme` folder still needs to be in your web root directory, example: `/var/www/html/theme` even if you are using auto indexing for a sub directory like above example.
