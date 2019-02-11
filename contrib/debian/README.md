
Debian
====================
This directory contains files used to package ultrapaycoind/ultrapaycoin-qt
for Debian-based Linux systems. If you compile ultrapaycoind/ultrapaycoin-qt yourself, there are some useful files here.

## ultrapaycoin: URI support ##


ultrapaycoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install ultrapaycoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your ultrapaycoinqt binary to `/usr/bin`
and the `../../share/pixmaps/ultrapaycoin128.png` to `/usr/share/pixmaps`

ultrapaycoin-qt.protocol (KDE)

