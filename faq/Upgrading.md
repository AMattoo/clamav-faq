# Upgrading ClamAV #

# Upgrade Instructions #

## Packages ##

If you installed from packages, find new packages and install them. See ClamPackages.
If there are no new packages, you have three options:

* Wait
* Build Clam Package
* Install From Source

## Sources ##

If you installed from sources, first uninstall the old version:

`./configure`
`sudo make uninstall`

Compile and install the new one: see [Installing ClamAV]

#### Note: ####
* Depending on your installation method, you might want to backup configuration (located in _/usr/local/etc_ by default) and signature database (located in _/usr/local/share/clamav_ by default). Don't forget to restore backups before starting up updated ClamAV.
* Backup your database signature (located in _/usr/local/share/clamav_ by default) before upgrading to newer ClamAV version. Restore the backed up database signature before running the updated version. This is to avoid getting the _/usr/local/share/clamav not locked_ error message when doing _freshclam_.

## Webmin and yum ##

If you obtained a server from a competent hosting provider they probably already installed clamav using yum and the extras repository. To obtain a new version:

`yum list clamav

yum update clamav` (if everything updated properly, run freshclam)

[Installing ClamAV]: https://github.com/vrtadmin/clamav-faq/blob/master/faq/Installing.md

[Upgrade Instructions]: https://github.com/vrtadmin/clamav-faq/blob/master/faq/Upgrading.md
