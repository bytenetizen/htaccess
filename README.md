# htaccess

RewriteCond %{REQUEST_URI} ^/player(.*)
RewriteRule (.*) /pl/index.php [L]


#facebook 404
#URL применения
RewriteCond %{REQUEST_URI} ^/actions/|(/music/)|(/playlist/)|(/online/)
#Удалить все из URL
#RewriteCond %{QUERY_STRING} ^(.+) [NC]
#Удалить fbclid из URL
RewriteCond %{QUERY_STRING} ^(.*)fbclid=[^&]+(.*)$ [NC]
RewriteRule ^(.*)$ /$1? [R=301,L]
