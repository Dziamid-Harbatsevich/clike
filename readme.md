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

NOTE: The passwords should be saved encoded according to ASCII Codes Table (% + Hex code of the character, "%26" = "&").
[ASCII Table](https://ascii.cl/)

Examples:
* clike git:commit [-c]