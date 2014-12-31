# GUID

# Official Repository

## Add My PPA
sudo add-apt-repository ppa:danielheth/guid
sudo apt-get update

## Installing guid
sudo apt-get install guid


## Launch Daemon
sudo guidd

## Test Client
guid


## Uninstall guid
sudo apt-get remove guid





# Development Notes
Interesting reads:
https://launchpad.net/~/
http://packaging.ubuntu.com/html/packaging-new-software.html
http://askubuntu.com/questions/90764/how-do-i-create-a-deb-package-for-a-single-python-script


## Development Process

### Increment Version
Copy the latest version "cp -R guid-X.X guid-Y.Y", so we have something to build from.

### Code
Update the code within guid-Y.Y as desired by adding features aor bugfixes, etc...

### Install Files List
Update the guid-Y.Y/debian/install file whenever there are new files to be put on the users system.


## Publishing
We must officially build/sign the project by running "debuild -S -k[signing key id]" from within the guid-Y.Y folder.  This will step through the build process, troubleshoot any errors.

## Upload/Push to PPA
From the root project folder run "dput ppa:danielheth/guid guid_Y.Y_source.changes"

After publishing, that adds the Y.Y version to the build queue and you receive an email indicating the build was accepted.

It can take a while (tests show 5-10min) for the build to complete and the new package to appear properly published on the launchpad site.  However it may take 10-20min for it to because updatable using apt-get on endpoints that have guid installed.


