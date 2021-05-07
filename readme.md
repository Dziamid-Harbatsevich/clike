# FEATURES #
* Server Management
* Git Add, Commit and Push
* Tar Backup and Copy to Storage

# COMPATABILITY #
Developed and tested on Ubuntu 20.04 / PHP 8.0.5 / Nginx / MySQL

# CLIKE INSTALLATION #

### Clone app ###
In some [app_folder] defined by you. Just check if you have an appropriate rights to use this folder.

### Create an alias for clike command in ~/.bash_aliases: ###
alias clike='php ~/[app_folder]/clike'

### Set PHP version running ###
Check files: "webserver/devserv", "webserver/devserv-min"

# Server Management #
### Commands ###
clike server:(start|stop|reload... "common parameters for Nginx, PHP, Mysql according to documentation") [--min]
--min control servers accept mysql (Nginx+PHP only)

Examples:
* clike server:start
* clike server:reload [--min]

# Git Control #

Configure connection to the GitHub repository in .env file.
"GIT_HOST" parameter equals a host + full path to the git repository root.
If you wish to get total automatization than set "GIT_AUTOPASS" to true and set password. Please, consider notification below as the Git credentials send via URL-HTTPS.

NOTE: The passwords should be saved encoded according to ASCII Codes Table (% + Hex code of the character, "%26" = "&").
[ASCII Table](https://ascii.cl/)

Default master branch named as "master". You can choose your own branch and gitfile format ("origin" is conventional) while pushing new commits.

Examples:
* clike git:commit [-c "Commit text.."]