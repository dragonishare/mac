[Install MySQL on macOS Sierra](https://gist.github.com/nrollr/3f57fc15ded7dddddcc4e82fe137b58e)

Load and start the MySQL service : `$ brew services start mysql`

Check of the MySQL service has been loaded : `$ brew services list`

Verify the installed MySQL instance : `$ mysql -V.`


Open Terminal and execute the following command to set the root password:
`mysqladmin -u root password 'yourpassword'`


