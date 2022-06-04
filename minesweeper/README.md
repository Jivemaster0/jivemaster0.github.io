# Minesweeper


## Links

	https://slicker.me/javascript/minesweeper/minesweeper.htm

## Apache alias

Creating file /etc/apache2/sites-available/aa-minesweeper.conf with the
following content:

<IfModule alias_module>
   Alias "/minesweeper/" "/opt/alianwar/minesweeper/webroot/"
   <Directory "/opt/alianwar/minesweeper/webroot">
      Options Indexes FollowSymLinks Multiviews
      AllowOverride None
      Require all granted
   </Directory>
</IfModule>

Enable, test and reload the web server configuration

sudo a2ensite aa-minesweeper.conf
sudo apachectl configtest
sudo systemctl reload apache2

URL is http://localhost/minesweeper/
Note the "/" at the end is important.

## History

20210109 : Created this page.
20210131 : Added the alias information.
