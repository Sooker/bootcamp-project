server {
        root /home/bejenari/bootcamp-project/public;
        index index.php index.html index.htm index.nginx-debian.html;
        server_name daniil.md;
        access_log /var/log/nginx/daniil.md.access.log;
        error_log /var/log/nginx/daniil.md.error.log;
        location / {
                try_files $uri $uri/ /index.php$is_args$args;
        }
        charset utf-8;
        large_client_header_buffers 8 64k;
        client_max_body_size 20M;
}
