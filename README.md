# htaccess

RewriteCond %{REQUEST_URI} ^/player(.*)
RewriteRule (.*) /pl/index.php [L]
