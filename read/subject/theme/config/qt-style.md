---
title: 設定「Qt Style」
nav_order: 3101
has_children: false
parent: 設定
grand_parent: 佈景主題
---


# 設定「Qt Style」


## 主題

* [lxqt-config-appearance](#lxqt-config-appearance)
* [環境變數](#環境變數)
* [設定「Qt Style」採用「kvantum」](#設定qt-style採用kvantum)
* [設定「Qt Style」採用「gtk2」](#設定qt-style採用gtk2)


## lxqt-config-appearance

理論上，透過「`lxqt-config-appearance` (LXQt Appearance Configuaration)」這個「圖形介面程式」來操作

在「Widget Style」這個這個頁面，

有一個選項「Qt Style」，有一個下拉選單，預設有以下三個選項可選

* Breeze
* Windows
* Fusion

預設是採用「Breeze」。

這個「設定值」，會被保存在「[~/.config/lxqt/lxqt.conf](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/lxqt-config/Main/asset/overlay/etc/skel/.config/lxqt/lxqt.conf#L18)」這個檔案，內容類似如下。

``` ini
[Qt]
style=Breeze
```

不過測試過程中，發現這個機制好像還沒有實做得很完善，

所以我們回歸到「環境變數」這個方式來設定，


## 環境變數

執行

``` sh
env | grep QT
```

顯示

``` sh
QT_ACCESSIBILITY=1
SAL_VCL_QT5_USE_CAIRO=true
LXQT_SESSION_CONFIG=session
QT_QPA_PLATFORMTHEME=lxqt
QT_STYLE_OVERRIDE=Breeze
QT_IM_MODULE=fcitx
QT_PLATFORM_PLUGIN=lxqt
```

在設定「Qt Style」這個議題，我們關注的是其中兩行如下

``` sh
QT_QPA_PLATFORMTHEME=lxqt
QT_STYLE_OVERRIDE=Breeze
```


## 設定「Qt Style」採用「kvantum」

執行下面指令，安裝「[qt5-style-kvantum](https://packages.ubuntu.com/noble/qt5-style-kvantum)」

``` sh
sudo apt-get install qt5-style-kvantum
```

安裝完畢後，

重新執行「`lxqt-config-appearance` (LXQt Appearance Configuaration)」這個「圖形介面程式」，

在「Widget Style」這個這個頁面，

在選項「Qt Style」的下拉選單，

就會多出「`kvantum`」和「`kvantum-dark`」兩個選項

* Breeze
* kvantum-dark
* kvantum
* Windows
* Fusion

上面提到這個機制好像還沒有實做得很完善，

所以我們回歸到「環境變數」這個方式來設定，

於是我們可以透過「`lxqt-config-session` (LXQt Session Settings)」這個「圖形介面程式」來操作。

在「Environment (Advanced)」這個頁面，

我們可以新增一個「環境變數」，

名稱是「`QT_STYLE_OVERRIDE`」，

設定值填入「`kvantum`」

這個設定值，會被保存在「[~/.config/lxqt/session.conf](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/lxqt/session.conf#L9)」這個檔案，內容類似如下

``` ini
[Environment]
QT_STYLE_OVERRIDE=kvantum
```

在設定「kvantum」要採用的「佈景主題」前，

我們先執行下面的指令，安裝「[arc-kde](https://packages.ubuntu.com/noble/arc-kde)」

``` sh
sudo apt-get install arc-kde
```

因為「arc-kde」這個「Package」，有包含我們要舉例的「佈景主題」

執行

``` sh
dpkg -L arc-kde | grep -i kvantum
```

顯示

```
/usr/share/Kvantum
/usr/share/Kvantum/Arc
/usr/share/Kvantum/Arc/AUTHORS
/usr/share/Kvantum/Arc/Arc.kvconfig
/usr/share/Kvantum/Arc/Arc.svg
/usr/share/Kvantum/ArcDark
/usr/share/Kvantum/ArcDark/AUTHORS
/usr/share/Kvantum/ArcDark/ArcDark.kvconfig
/usr/share/Kvantum/ArcDark/ArcDark.svg
/usr/share/Kvantum/ArcDarker
/usr/share/Kvantum/ArcDarker/AUTHORS
/usr/share/Kvantum/ArcDarker/ArcDarker.kvconfig
/usr/share/Kvantum/ArcDarker/ArcDarker.svg
```

也就是有下面三個「kvantum」佈景主題

* Arc
* ArcDark
* ArcDarker

接著我們可以透過「`kvantummanager` (Kvantum Manager)」這個「圖形介面程式」來設定「kvantum」要採用的「佈景主題」，

在「Change/Delete Theme」這個頁面，可以設定。

這裡我們舉例，採用「ArcDark」這個「kvantum」佈景主題。

這個設定值，會被保存在「[~/.config/Kvantum/kvantum.kvconfig](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/Kvantum/kvantum.kvconfig)」這個檔案，

執行下面指令，觀看「~/.config/Kvantum/kvantum.kvconfig」這個檔案的內容

``` sh
cat ~/.config/Kvantum/kvantum.kvconfig
```

顯示

``` ini
[General]
theme=ArcDark
```

最後只要重新登出登入，設定「Qt Style」採用「kvantum」就會生效。

爾後只要透過「`kvantummanager` (Kvantum Manager)」這個「圖形介面程式」來設定「kvantum」要採用的「佈景主題」。


## 設定「Qt Style」採用「gtk2」

執行下面指令，安裝「[qt5-style-plugins](https://packages.ubuntu.com/noble/qt5-style-plugins)」

``` sh
sudo apt-get install qt5-style-plugins
```

就會安裝下面四個「Package」

* [qt5-gtk2-platformtheme](https://packages.ubuntu.com/noble/qt5-gtk2-platformtheme)
* [qt5-style-plugin-cleanlooks](https://packages.ubuntu.com/noble/qt5-style-plugin-cleanlooks)
* [qt5-style-plugin-motif](https://packages.ubuntu.com/noble/)
* [qt5-style-plugin-plastique](https://packages.ubuntu.com/noble/qt5-style-plugin-motif)


安裝完畢後，

重新執行「`lxqt-config-appearance` (LXQt Appearance Configuaration)」這個「圖形介面程式」，

在「Widget Style」這個這個頁面，

在選項「Qt Style」的下拉選單，

就會多出「`cleanlooks`」，「`gtk2`」，「`cde`」，「`motif`」，「`plastique`」這幾個選項

* Breeze
* kvantum-dark
* kvantum
* cleanlooks
* gtk2
* cde
* motif
* plastique
* Windows
* Fusion

如同上面設定「Qt Style」採用「kvantum」提到的，

我們回歸到「環境變數」的作法

只要設定「`QT_STYLE_OVERRIDE=gtk2`」就行了。

這樣「Qt Style」就會跟隨「gtk2」的設定。

由於在「lubuntu」我們並沒有起任何「xsettings」的「Server」，

所以「gtk2」和「gtk3」就會採用「設定檔」的設定

| gtk | 設定檔 |
| --- | --- |
| gtk2 | [~/.gtkrc-2.0](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.gtkrc-2.0#L8) |
| gtk3 | [~/.config/gtk-3.0/settings.ini](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/gtk-3.0/settings.ini#L11) |

我們除了可以直接編輯這兩個檔案。

也可以透過「`lxqt-config-appearance` (LXQt Appearance Configuaration)」這個「圖形介面程式」來設定，

在「Gtk Style」這個這個頁面，就可以設定。


## 相關的佈景主題

* [arc-theme](https://packages.ubuntu.com/noble/arc-theme)
* [arc-kde](https://packages.ubuntu.com/noble/arc-kde)
