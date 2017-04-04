sNaglite
========

Fork of the status monitor Naglite3 for a NOC or operations room. This version is modified to be used with the SNAG-View 3 Monitoring Suite.

Originally written by Steffen Zieger <me@saz.sh>.
Licensed under the GPL.

In case of any problems or bug fixes, feel free open an issue in this repository.

Requirements
------------

sNaglite is only functional with SNAG-View 3.5 and above.

- Web server of your choice with PHP support
- PHP 5.2 or newer
- git

sNaglite must be installed on the same host where SNAG-View 3 is running, as it
needs to read status.dat from Nagios.

Installation
------------

1. Switch to a directory accessible through your web server (e.g. /opt/snagview/frontend/).
2. `git clone https://github.com/SectorNordAG/sNaglite.git snaglite`
3. Copy config.php.example to config.php if you need to change a setting.
4. Open a browser and point it to https://snag.view.server/snaglite/index.php.

Customization
-------------

For all possible config options have a look at config.php.example

### CSS

If you want to change colors, create a file called 'custom.css' in the
directory where sNaglite is placed and add your changes.

If you want to use a per site css, just pass the GET-parameter "css" pointing to a local file.
e.g. http://your-host/snaglite/index.php?css=my_custom_css

#### Dashboard CSS

To show the naglite screen in a manner that's readable from a few feet away, you can use the builtin dashboard stylesheet.
e.g. http://your-host/snaglite/index.php?css=dashboard

### Refresh interval

You can change the refresh interval (in seconds) through a GET parameter, too.

Example:
http://your-host/snaglite/index.php?refresh=100
