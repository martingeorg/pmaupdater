# pmaupdater
phpMyAdmin Updater

Script for automatically installing the/updating to latest phpMyAdmin version.

This Bash script will do the following.

* Remove any old phpMyAdmin files (in the current folder) if there are any.
* Download the latest version of phpMyAdmin from phpMyAdmin site.
* Extract the downloaded `.tar.gz` file in the current folder.
* Copy `config.sample.inc.php` to `config.inc.php`.
* Automatically update the `'blowfish_secret'` in `config.inc.php` using an `md5sum` of 512 bytes received from `/dev/urandom`.
* Clean up by removing the downloaded `.tar.gz` file

To use it, simply drop the following commands in your terminal.

`git clone https://github.com/martingeorg/pmaupdater.git && (cd pmaupdater && ./pmaupdater)`

or

`wget https://github.com/martingeorg/pmaupdater/archive/master.zip -O pmaupdater.zip && unzip -j ./pmaupdater.zip pmaupdater-master/* -d pmaupdater && (cd pmaupdater && ./pmaupdater)`

###### Make sure you don't have already a file or folder with the name `pmaupdater.zip` or `pmaupdater` as it will be overwritten!
