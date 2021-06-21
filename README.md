# extenstion-hide-and-folder-access-deny

For hideing PHP File Extension 
Create .htaccess file and paste below code

# Run Php without filename extension
RewriteEngine on
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME}.php -f
RewriteRule ^(.*)$ $1.php

# Return 404 if original request is .php
RewriteCond %{THE_REQUEST} "^[^ ]* .*?\.php[? ].*$"
RewriteRule .* - [L,R=404]



For deny folder access  
Create .htaccess file on that folder and paste below code

Options -Indexes
