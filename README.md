# nginx-autoindex-theme
A simple theme for nginx for autoindexed directories

## How to use

Create a directory called `theme` under your nginx root directory, defaul is `/var/www/html` so the theme directory will be located in `/var/www/html/theme`

Add indexing to your directory
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
