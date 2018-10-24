# htaccess

RewriteCond %{REQUEST_URI} ^/player(.*)
RewriteRule (.*) /pl/index.php [L]


#facebook 404
RewriteCond %{REQUEST_URI} ^/actions/|(/music/)|(/playlist/)|(/online/)
#RewriteCond %{QUERY_STRING} ^(.+) [NC]
RewriteCond %{QUERY_STRING} ^(.*)fbclid=[^&]+(.*)$ [NC]
RewriteRule ^(.*)$ /$1? [R=301,L]
