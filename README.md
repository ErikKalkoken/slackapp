# slackapp

## Description
The PHP script `install.php` is a rudimentary example for installing a self developed Slack app using OAuth into a Slack team.

## Requirements
In order to use this script you need a webserver with PHP 5 that is accessable from the Internet. SSL is technically not required, howwever strongly recommended for security reasons.
This script will run standalone and does not require any additional libraries.

## How to use it
### 1. Create your own Slack app

### 2. Update your Slack app settings

- Set the redirect URL to the location of your install script, e.g. http://www.myserver.net/apps/myapp/install.php

### 3. Update install.php with your custom settings.
* `$client_id`, `client_secret`: You will find them in the administration settings of your app under "Basic Information".
* `APP_TITLE`: A title of your choosing
* `$scope`: list of requested scopes for your app, e.g. `"commands,bot"`

### 4. Deploy the script to your webserver

- Upload the script to your webserver, e.g. with FTP to /apps/myapp on www.myserver.net

That's it. Now you can open your install script from a webbrowser and click on the "Add to Slack" button to install it.

## Additional remarks
The aim of this script was to provide a simple solution to install a Slack app. It should be sufficient for private and educational use. If you want to use it for Slack apps that are available in the Slack App Directory I would suggest to consider the following changes:
* Use HTTPS instead of HTTP to protect your client secret
* Move client_id and client_secret to a config file
* Move detailed error messages to a logfile and replace error messages with a more user friendly version

