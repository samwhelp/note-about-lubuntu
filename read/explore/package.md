---
title: Package
nav_order: 1000
has_children: true
parent: 探索
---


# Package


## 主題

* [Explore Package List](#explore-package-list)
* [Lxqt / Explore](#lxqt--explore)
* [Lxqt / Package List](#lxqt--package-list)
* [Lubuntu / Explore](#lubuntu--explore)
* [Lubuntu / Package List](#lubuntu--package-list)


## Explore Package List

| Package | Explore |
| --- | --- |
| [lxqt-config](https://packages.ubuntu.com/noble/lxqt-config) | [Explore](package/lxqt-config) |




## Lxqt / Explore

執行

``` sh
apt-cache search lxqt | sort -u
```

顯示

```
calamares-settings-lubuntu - Lubuntu Calamares Settings and Branding
liblxqt-globalkeys-ui1 - daemon used to register global keyboard shortcuts (ui files)
liblxqt-globalkeys-ui1-dev - daemon used to register global keyboard shortcuts (ui dev files)
liblxqt-globalkeys1 - daemon used to register global keyboard shortcuts (shared libs)
liblxqt-globalkeys1-dev - daemon used to register global keyboard shortcuts (dev files)
liblxqt-l10n - Language package for liblxqt
liblxqt1 - Shared libraries for LXQt desktop environment (libs)
liblxqt1-dev - Shared libraries for LXQt desktop environment (dev)
libqt5xdg-dev - Development files for libqtxdg
libqt5xdg3 - Implementation of the XDG Specifications for Qt (shared lib)
libqt5xdgiconloader-dev - Development files for libqtxdgiconloader
libqt5xdgiconloader3 - Implementation of the XDG Iconloader for Qt (shared lib)
libqtilitools-dev - Qtilitools library package
lubuntu-artwork - artwork for Lubuntu
lubuntu-installer-prompt - Live ISO prompt for trying or installing Lubuntu
lximage-qt - Image viewer for LXQt
lximage-qt-l10n - Language-package for lximage-qt
lxqt - Metapackage for LXQt
lxqt-about - About screen for LXQt
lxqt-about-l10n - Language package for lxqt-about
lxqt-admin - Admin tools for LXQt
lxqt-admin-l10n - Language package for lxqt-admin
lxqt-archiver - Archive Manager for LXQt
lxqt-archiver-l10n - Language package for lxqt-archiver
lxqt-branding-debian - Debian branding for LXQt
lxqt-build-tools - Build tools for the LXQt desktop environment
lxqt-config - LXQt system settings center
lxqt-config-l10n - Language package for lxqt-config
lxqt-core - Metapackage for the LXQt core
lxqt-globalkeys - daemon used to register global keyboard shortcuts (appl.)
lxqt-globalkeys-l10n - Language package for lxqt-globalkeys
lxqt-menu-data - Freedesktop.org compliant menu files for LXQt
lxqt-notificationd - LXQt notification daemon
lxqt-notificationd-l10n - Language package for lxqt-notificationd
lxqt-openssh-askpass - OpenSSH user/password GUI dialog for LXQt
lxqt-openssh-askpass-l10n - Language package for lxqt-openssh-askpass
lxqt-panel - LXQt desktop panel
lxqt-panel-l10n - Language package for lxqt-panel
lxqt-policykit - LXQt authentication agent for PolicyKit
lxqt-policykit-l10n - Language package for lxqt-policykit
lxqt-powermanagement - power management module for LXQt
lxqt-powermanagement-l10n - Language package for lxqt-powermanagement
lxqt-qtplugin - LXQt system integration plugin for Qt
lxqt-runner - LXQt program launcher
lxqt-runner-l10n - Language package for lxqt-runner
lxqt-session - session manager component for LXQt
lxqt-session-l10n - Language package for lxqt-session
lxqt-sudo - Graphical Qt frontend for plain sudo
lxqt-sudo-l10n - Language package for lxqt-sudo
lxqt-system-theme - System theme for LXQt
lxqt-theme-debian - Debian theme for LXQt
lxqt-themes - Themes for LXQt
lxqt-themes-extra - Extra LXQt Themes
pavucontrol-qt - Qt port of volume control pavucontrol
qt5-style-kvantum - Kvantum style engine (binaries)
qt5-style-kvantum-l10n - Kvantum style engine (localization)
qt5-style-kvantum-themes - Kvantum style engine (themes)
qtxdg-tools - User tools for libqtxdg
task-lxqt-desktop - LXQt
xdg-desktop-portal-lxqt - xdg-desktop-portal using Qt/KF5/libfm-qt
zulusafe-cli - cli that manages encrypted volumes
```


執行

``` sh
dpkg -l '*lxqt*'
```

顯示

```
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name                         Version        Architecture Description
+++-============================-==============-============-===============================================================
un  liblxqt-globalkeys-ui0       <none>         <none>       (no description available)
ii  liblxqt-globalkeys-ui1:amd64 1.4.0-0ubuntu1 amd64        daemon used to register global keyboard shortcuts (ui files)
un  liblxqt-globalkeys0          <none>         <none>       (no description available)
ii  liblxqt-globalkeys1:amd64    1.4.0-0ubuntu1 amd64        daemon used to register global keyboard shortcuts (shared libs)
ii  liblxqt-l10n                 1.4.0-0ubuntu1 all          Language package for liblxqt
un  liblxqt0                     <none>         <none>       (no description available)
ii  liblxqt1                     1.4.0-0ubuntu1 amd64        Shared libraries for LXQt desktop environment (libs)
un  lxqt                         <none>         <none>       (no description available)
ii  lxqt-about                   1.4.0-0ubuntu1 amd64        About screen for LXQt
ii  lxqt-about-l10n              1.4.0-0ubuntu1 all          Language package for lxqt-about
ii  lxqt-admin                   1.4.0-0ubuntu1 amd64        Admin tools for LXQt
ii  lxqt-admin-l10n              1.4.0-0ubuntu1 all          Language package for lxqt-admin
ii  lxqt-archiver                0.9.0-0ubuntu1 amd64        Archive Manager for LXQt
ii  lxqt-archiver-l10n           0.9.0-0ubuntu1 all          Language package for lxqt-archiver
un  lxqt-branding                <none>         <none>       (no description available)
un  lxqt-branding-debian         <none>         <none>       (no description available)
un  lxqt-common                  <none>         <none>       (no description available)
ii  lxqt-config                  1.4.0-0ubuntu2 amd64        LXQt system settings center
ii  lxqt-config-l10n             1.4.0-0ubuntu2 all          Language package for lxqt-config
ii  lxqt-core                    30ubuntu2      all          Metapackage for the LXQt core
ii  lxqt-globalkeys              1.4.0-0ubuntu1 amd64        daemon used to register global keyboard shortcuts (appl.)
ii  lxqt-globalkeys-l10n         1.4.0-0ubuntu1 all          Language package for lxqt-globalkeys
ii  lxqt-menu-data               1.4.1-0ubuntu4 all          Freedesktop.org compliant menu files for LXQt
ii  lxqt-notificationd           1.4.0-0ubuntu1 amd64        LXQt notification daemon
ii  lxqt-notificationd-l10n      1.4.0-0ubuntu1 all          Language package for lxqt-notificationd
ii  lxqt-openssh-askpass         1.4.0-0ubuntu1 amd64        OpenSSH user/password GUI dialog for LXQt
ii  lxqt-openssh-askpass-l10n    1.4.0-0ubuntu1 all          Language package for lxqt-openssh-askpass
ii  lxqt-panel                   1.4.0-0ubuntu2 amd64        LXQt desktop panel
ii  lxqt-panel-l10n              1.4.0-0ubuntu2 all          Language package for lxqt-panel
ii  lxqt-policykit               1.4.0-0ubuntu1 amd64        LXQt authentication agent for PolicyKit
ii  lxqt-policykit-l10n          1.4.0-0ubuntu1 all          Language package for lxqt-policykit
ii  lxqt-powermanagement         1.4.0-0ubuntu2 amd64        power management module for LXQt
ii  lxqt-powermanagement-l10n    1.4.0-0ubuntu2 all          Language package for lxqt-powermanagement
ii  lxqt-qtplugin:amd64          1.4.0-0ubuntu2 amd64        LXQt system integration plugin for Qt
ii  lxqt-runner                  1.4.0-0ubuntu1 amd64        LXQt program launcher
ii  lxqt-runner-l10n             1.4.0-0ubuntu1 all          Language package for lxqt-runner
ii  lxqt-session                 1.4.0-0ubuntu3 amd64        session manager component for LXQt
ii  lxqt-session-l10n            1.4.0-0ubuntu3 all          Language package for lxqt-session
ii  lxqt-sudo                    1.4.0-0ubuntu2 amd64        Graphical Qt frontend for plain sudo
ii  lxqt-sudo-l10n               1.4.0-0ubuntu2 all          Language package for lxqt-sudo
ii  lxqt-system-theme            1.3.0-0ubuntu1 all          System theme for LXQt
un  lxqt-theme                   <none>         <none>       (no description available)
ii  lxqt-themes                  1.3.0-0ubuntu1 all          Themes for LXQt
ii  lxqt-themes-extra            1.0-0ubuntu1   all          Extra LXQt Themes
ii  xdg-desktop-portal-lxqt      0.5.0-0ubuntu2 amd64        xdg-desktop-portal using Qt/KF5/libfm-qt
```


執行

``` sh
dpkg -l '*lxqt*' | grep -E '^ii|^un' | awk '{printf $2"\n"}'
```

顯示

```
liblxqt-globalkeys-ui0
liblxqt-globalkeys-ui1:amd64
liblxqt-globalkeys0
liblxqt-globalkeys1:amd64
liblxqt-l10n
liblxqt0
liblxqt1
lxqt
lxqt-about
lxqt-about-l10n
lxqt-admin
lxqt-admin-l10n
lxqt-archiver
lxqt-archiver-l10n
lxqt-branding
lxqt-branding-debian
lxqt-common
lxqt-config
lxqt-config-l10n
lxqt-core
lxqt-globalkeys
lxqt-globalkeys-l10n
lxqt-menu-data
lxqt-notificationd
lxqt-notificationd-l10n
lxqt-openssh-askpass
lxqt-openssh-askpass-l10n
lxqt-panel
lxqt-panel-l10n
lxqt-policykit
lxqt-policykit-l10n
lxqt-powermanagement
lxqt-powermanagement-l10n
lxqt-qtplugin:amd64
lxqt-runner
lxqt-runner-l10n
lxqt-session
lxqt-session-l10n
lxqt-sudo
lxqt-sudo-l10n
lxqt-system-theme
lxqt-theme
lxqt-themes
lxqt-themes-extra
xdg-desktop-portal-lxqt
```



執行

``` sh
dpkg -l '*lxqt*' | grep -E '^ii' | awk '{printf $2"\n"}'
```

顯示

```
liblxqt-globalkeys-ui1:amd64
liblxqt-globalkeys1:amd64
liblxqt-l10n
liblxqt1
lxqt-about
lxqt-about-l10n
lxqt-admin
lxqt-admin-l10n
lxqt-archiver
lxqt-archiver-l10n
lxqt-config
lxqt-config-l10n
lxqt-core
lxqt-globalkeys
lxqt-globalkeys-l10n
lxqt-menu-data
lxqt-notificationd
lxqt-notificationd-l10n
lxqt-openssh-askpass
lxqt-openssh-askpass-l10n
lxqt-panel
lxqt-panel-l10n
lxqt-policykit
lxqt-policykit-l10n
lxqt-powermanagement
lxqt-powermanagement-l10n
lxqt-qtplugin:amd64
lxqt-runner
lxqt-runner-l10n
lxqt-session
lxqt-session-l10n
lxqt-sudo
lxqt-sudo-l10n
lxqt-system-theme
lxqt-themes
lxqt-themes-extra
xdg-desktop-portal-lxqt
```



執行

``` sh
dpkg --get-selections | grep lxqt
```

顯示

```
liblxqt-globalkeys-ui1:amd64			install
liblxqt-globalkeys1:amd64			install
liblxqt-l10n					install
liblxqt1					install
lxqt-about					install
lxqt-about-l10n					install
lxqt-admin					install
lxqt-admin-l10n					install
lxqt-archiver					install
lxqt-archiver-l10n				install
lxqt-config					install
lxqt-config-l10n				install
lxqt-core					install
lxqt-globalkeys					install
lxqt-globalkeys-l10n				install
lxqt-menu-data					install
lxqt-notificationd				install
lxqt-notificationd-l10n				install
lxqt-openssh-askpass				install
lxqt-openssh-askpass-l10n			install
lxqt-panel					install
lxqt-panel-l10n					install
lxqt-policykit					install
lxqt-policykit-l10n				install
lxqt-powermanagement				install
lxqt-powermanagement-l10n			install
lxqt-qtplugin:amd64				install
lxqt-runner					install
lxqt-runner-l10n				install
lxqt-session					install
lxqt-session-l10n				install
lxqt-sudo					install
lxqt-sudo-l10n					install
lxqt-system-theme				install
lxqt-themes					install
lxqt-themes-extra				install
xdg-desktop-portal-lxqt				install
```


## Lxqt / Package List


執行

``` sh
dpkg -l '*lxqt*' | grep -E '^ii|^un' | awk '{printf "| ["$2"](https://packages.ubuntu.com/noble/"$2") |\n"}'
```




執行

``` sh
dpkg -l '*lxqt*' | grep -E '^ii|^un' | awk '{print $2}' | awk -F ':' '{printf "| ["$1"](https://packages.ubuntu.com/noble/"$1") |\n"}'
```

| Package |
| ------- |
| [liblxqt-globalkeys-ui0](https://packages.ubuntu.com/noble/liblxqt-globalkeys-ui0) |
| [liblxqt-globalkeys-ui1](https://packages.ubuntu.com/noble/liblxqt-globalkeys-ui1) |
| [liblxqt-globalkeys0](https://packages.ubuntu.com/noble/liblxqt-globalkeys0) |
| [liblxqt-globalkeys1](https://packages.ubuntu.com/noble/liblxqt-globalkeys1) |
| [liblxqt-l10n](https://packages.ubuntu.com/noble/liblxqt-l10n) |
| [liblxqt0](https://packages.ubuntu.com/noble/liblxqt0) |
| [liblxqt1](https://packages.ubuntu.com/noble/liblxqt1) |
| [lxqt](https://packages.ubuntu.com/noble/lxqt) |
| [lxqt-about](https://packages.ubuntu.com/noble/lxqt-about) |
| [lxqt-about-l10n](https://packages.ubuntu.com/noble/lxqt-about-l10n) |
| [lxqt-admin](https://packages.ubuntu.com/noble/lxqt-admin) |
| [lxqt-admin-l10n](https://packages.ubuntu.com/noble/lxqt-admin-l10n) |
| [lxqt-archiver](https://packages.ubuntu.com/noble/lxqt-archiver) |
| [lxqt-archiver-l10n](https://packages.ubuntu.com/noble/lxqt-archiver-l10n) |
| [lxqt-branding](https://packages.ubuntu.com/noble/lxqt-branding) |
| [lxqt-branding-debian](https://packages.ubuntu.com/noble/lxqt-branding-debian) |
| [lxqt-common](https://packages.ubuntu.com/noble/lxqt-common) |
| [lxqt-config](https://packages.ubuntu.com/noble/lxqt-config) |
| [lxqt-config-l10n](https://packages.ubuntu.com/noble/lxqt-config-l10n) |
| [lxqt-core](https://packages.ubuntu.com/noble/lxqt-core) |
| [lxqt-globalkeys](https://packages.ubuntu.com/noble/lxqt-globalkeys) |
| [lxqt-globalkeys-l10n](https://packages.ubuntu.com/noble/lxqt-globalkeys-l10n) |
| [lxqt-menu-data](https://packages.ubuntu.com/noble/lxqt-menu-data) |
| [lxqt-notificationd](https://packages.ubuntu.com/noble/lxqt-notificationd) |
| [lxqt-notificationd-l10n](https://packages.ubuntu.com/noble/lxqt-notificationd-l10n) |
| [lxqt-openssh-askpass](https://packages.ubuntu.com/noble/lxqt-openssh-askpass) |
| [lxqt-openssh-askpass-l10n](https://packages.ubuntu.com/noble/lxqt-openssh-askpass-l10n) |
| [lxqt-panel](https://packages.ubuntu.com/noble/lxqt-panel) |
| [lxqt-panel-l10n](https://packages.ubuntu.com/noble/lxqt-panel-l10n) |
| [lxqt-policykit](https://packages.ubuntu.com/noble/lxqt-policykit) |
| [lxqt-policykit-l10n](https://packages.ubuntu.com/noble/lxqt-policykit-l10n) |
| [lxqt-powermanagement](https://packages.ubuntu.com/noble/lxqt-powermanagement) |
| [lxqt-powermanagement-l10n](https://packages.ubuntu.com/noble/lxqt-powermanagement-l10n) |
| [lxqt-qtplugin](https://packages.ubuntu.com/noble/lxqt-qtplugin) |
| [lxqt-runner](https://packages.ubuntu.com/noble/lxqt-runner) |
| [lxqt-runner-l10n](https://packages.ubuntu.com/noble/lxqt-runner-l10n) |
| [lxqt-session](https://packages.ubuntu.com/noble/lxqt-session) |
| [lxqt-session-l10n](https://packages.ubuntu.com/noble/lxqt-session-l10n) |
| [lxqt-sudo](https://packages.ubuntu.com/noble/lxqt-sudo) |
| [lxqt-sudo-l10n](https://packages.ubuntu.com/noble/lxqt-sudo-l10n) |
| [lxqt-system-theme](https://packages.ubuntu.com/noble/lxqt-system-theme) |
| [lxqt-theme](https://packages.ubuntu.com/noble/lxqt-theme) |
| [lxqt-themes](https://packages.ubuntu.com/noble/lxqt-themes) |
| [lxqt-themes-extra](https://packages.ubuntu.com/noble/lxqt-themes-extra) |
| [xdg-desktop-portal-lxqt](https://packages.ubuntu.com/noble/xdg-desktop-portal-lxqt) |




##  Lubuntu / Explore

執行

``` sh
apt-cache search lubuntu | sort -u
```

顯示

```
calamares-settings-lubuntu - Lubuntu Calamares Settings and Branding
grub2-themes-ubuntustudio - GRand Unified Bootloader, version 2 (Ubuntu Studio theme)
lubuntu-artwork - artwork for Lubuntu
lubuntu-default-settings - default settings for Lubuntu
lubuntu-desktop - Lubuntu Desktop environment
lubuntu-grub-theme - Theme for Lubuntu grub screen
lubuntu-installer-prompt - Live ISO prompt for trying or installing Lubuntu
lubuntu-restricted-addons - Commonly used restricted packages for Lubuntu
lubuntu-restricted-extras - Commonly used media codecs and fonts for Lubuntu (Transitional)
lubuntu-update-notifier - Lubuntu's update installer
plymouth-theme-lubuntu-logo - plymouth theme for Lubuntu
plymouth-theme-lubuntu-text - plymouth text theme for Lubuntu
sddm-theme-lubuntu - Lubuntu theme for SDDM X11 display manager
```


執行

``` sh
dpkg -l '*lubuntu*'
```

顯示

```
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name                        Version        Architecture Description
+++-===========================-==============-============-================================================
ii  calamares-settings-lubuntu  1:24.04.12     all          Lubuntu Calamares Settings and Branding
ii  lubuntu-artwork             24.04.3        all          artwork for Lubuntu
ii  lubuntu-default-settings    24.04.3        all          default settings for Lubuntu
ii  lubuntu-desktop             24.04.5        amd64        Lubuntu Desktop environment
ii  lubuntu-grub-theme          24.04.3        all          Theme for Lubuntu grub screen
ii  lubuntu-installer-prompt    1.1.2-0ubuntu1 amd64        Live ISO prompt for trying or installing Lubuntu
ii  lubuntu-update-notifier     1.0.0~alpha1   amd64        Lubuntu's update installer
ii  plymouth-theme-lubuntu-logo 24.04.3        all          plymouth theme for Lubuntu
ii  plymouth-theme-lubuntu-text 24.04.3        all          plymouth text theme for Lubuntu
ii  sddm-theme-lubuntu          24.04.3        all          Lubuntu theme for SDDM X11 display manager
```


##  Lubuntu / Package List

執行

``` sh
apt-cache search lubuntu | sort -u | awk -F ' - ' '{printf "| ["$1"](https://packages.ubuntu.com/noble/"$1") |\n"}'
```


| [calamares-settings-lubuntu](https://packages.ubuntu.com/noble/calamares-settings-lubuntu) |
| [grub2-themes-ubuntustudio](https://packages.ubuntu.com/noble/grub2-themes-ubuntustudio) |
| [lubuntu-artwork](https://packages.ubuntu.com/noble/lubuntu-artwork) |
| [lubuntu-default-settings](https://packages.ubuntu.com/noble/lubuntu-default-settings) |
| [lubuntu-desktop](https://packages.ubuntu.com/noble/lubuntu-desktop) |
| [lubuntu-grub-theme](https://packages.ubuntu.com/noble/lubuntu-grub-theme) |
| [lubuntu-installer-prompt](https://packages.ubuntu.com/noble/lubuntu-installer-prompt) |
| [lubuntu-restricted-addons](https://packages.ubuntu.com/noble/lubuntu-restricted-addons) |
| [lubuntu-restricted-extras](https://packages.ubuntu.com/noble/lubuntu-restricted-extras) |
| [lubuntu-update-notifier](https://packages.ubuntu.com/noble/lubuntu-update-notifier) |
| [plymouth-theme-lubuntu-logo](https://packages.ubuntu.com/noble/plymouth-theme-lubuntu-logo) |
| [plymouth-theme-lubuntu-text](https://packages.ubuntu.com/noble/plymouth-theme-lubuntu-text) |
| [sddm-theme-lubuntu](https://packages.ubuntu.com/noble/sddm-theme-lubuntu) |
