# Joomla Environment Stats

In order to better understand our install base and end user environments, this plugin has been created to send
those stats back to a Joomla controlled central server. No worries though, __no__ identifying data is captured
at any point, and we only keep latest data last sent to us so most data is dumped every 12 hours, after analysis and stat storage.

## Build Status
Travis-CI: [![Build Status](https://travis-ci.org/joomla-extensions/jstats-server.png)](https://travis-ci.org/joomla-extensions/jstats-server)
Scrutinizer-CI: [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/?branch=master) [![Code Coverage](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/?branch=master) [![Build Status](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/badges/build.png?b=master)](https://scrutinizer-ci.com/g/joomla-extensions/jstats-server/build-status/master)

## Installation

1. Clone this repo on your server into the folder **jstats-server**
2. Create a database called **jstats-server**
3. Run the sql file https://github.com/joomla-extensions/jstats-server/blob/master/etc/mysql.sql
4. Run ```composer install``` from the jstats-server folder to install the dependencies
5. Update the file etc/config.json with your database details if needed

## The Server

There are several requirements for running the JStats server

* mod_rewrite must be enabled
* AllowOverride All must be set in the Apache config in order for the .htaccess file to be used in the www folder
