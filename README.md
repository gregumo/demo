# Victoire demo (standard-project)

##Install

```
composer create-project victoire/demo myVictoire "1.0.*@dev"
```

##Domain names
Change domain names for yours in app/config/victoire_core.yml
```
    locale_pattern_table:
        demo.victoire.dev: fr
        demo.victoire.fr: fr
```

##Database
Create your database
```
php bin/console doctrine:database:create
```
And import the demo database with var/dump/db.sql

##Uploads
Extract demo uploads in web folder
```
tar -zxvf var/dump/uploads.tar.gz -C web/
```
##Bower
Install Bower packages
```
bower install
```
##Assets
If you have not already installed less, run the following command
```
npm install -g less
```
Then dump assets
```
php bin/console assets:install web --symlink
php bin/console mopa:bootstrap:symlink:less
php bin/console assetic:dump
```
##APC
*Careful* : please notice that Victoire needs APC in CLI mode. to do so, add these two lines in your php.ini config file

```ini
    apc.enabled = 1
    apc.enable_cli = 1
```
##Login page
Setup your virtualhost as usual and go to http://demo.victoire.dev/app_dev.php/login (assuming your local virtualhost is called demo.victoire.dev) and enter these credentials to start to test Victoire:

|Login|Password|
|-----|--------|
|`anakin@victoire.io`|test|

[https://github.com/Victoire/victoire](https://github.com/Victoire/victoire)
