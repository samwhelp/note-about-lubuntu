---
title: 設定「Lxqt」搭配「Kwin」
nav_order: 7032
has_children: false
parent: 設定「Lxqt」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Lxqt」搭配「Kwin」


## 微調腳本

| 微調腳本 |
| --- |
| [lxqt-with-kwin](https://github.com/samwhelp/lubuntu-adjustment/tree/main/prototype/main/alternative-config/lxqt-with-kwin/Main) |


## 前提

目前「Lubuntu」是採用「lxqt」這個「桌面環境」，

搭配「openbox」這個「視窗管理器」。

現在我們要來嘗試讓「lxqt」搭配「[kwin](https://samwhelp.github.io/note-about-lubuntu/read/master/window-manager/kwin.html)」。


## 操作步驟

* [安裝「Kwin」](#安裝kwin)
* [關於「Kwin」設定檔](#關於kwin設定檔)
* [設定「Window Decoration」](#設定window-decoration)


## 安裝「Kwin」

執行下面指令，安裝「kwin-x11」

``` sh
sudo apt-get install kwin-x11
```

因為我會使用到一些「Kwin Plugin」，所以執行下面指令，安裝「kwin-addons」

``` sh
sudo apt-get install kwin-addons
```

以上可以合併在一起，執行如下

``` sh
sudo apt-get install \
	kwin-x11 \
	kwin-addons

```




## 安裝「Kwin」設定檔

| 關於「Kwin」設定檔路徑 |
| --- |
| [~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc) |
| [~/.config/kactivitymanagerdrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kactivitymanagerdrc) |
| [~/.config/kwinrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kwinrc) |


| 關於「Kwin」設定檔路徑 |
| --- |
| [~/.config/kdeglobals](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kdeglobals) |
| [~/.config/plasmarc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/plasmarc) |
| [~/.config/kcminputrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kcminputrc) |
| [~/.config/kaccessrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kaccessrc) |



## 設定「Window Decoration」

在「Kwin」，「Window Decoration」預設使用的是「Breeze」

[設定片段](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kdedefaults/kwinrc#L16-L19)類似如下

``` sh
[org.kde.kdecoration2]
NoPlugin=false
library=org.kde.breeze
theme=Breeze
```

我們要改採用「Aurorae Theme」。

以下舉例，要採用「Arc-Dark」這個「Aurorae Theme」。

先執行下面指令，安裝「[arc-kde](https://packages.ubuntu.com/noble/arc-kde)」。

``` sh
sudo apt-get install arc-kde
```

執行

``` sh
dpkg -L arc-kde | grep aurorae
```

顯示

```
/usr/share/aurorae
/usr/share/aurorae/themes
/usr/share/aurorae/themes/Arc
/usr/share/aurorae/themes/Arc/AUTHORS
/usr/share/aurorae/themes/Arc/Arcrc
/usr/share/aurorae/themes/Arc/alldesktops.svg
/usr/share/aurorae/themes/Arc/close.svg
/usr/share/aurorae/themes/Arc/decoration.svg
/usr/share/aurorae/themes/Arc/keepabove.svg
/usr/share/aurorae/themes/Arc/keepbelow.svg
/usr/share/aurorae/themes/Arc/maximize.svg
/usr/share/aurorae/themes/Arc/metadata.desktop
/usr/share/aurorae/themes/Arc/minimize.svg
/usr/share/aurorae/themes/Arc/shade.svg
/usr/share/aurorae/themes/Arc-Dark
/usr/share/aurorae/themes/Arc-Dark/AUTHORS
/usr/share/aurorae/themes/Arc-Dark/Arc-Darkrc
/usr/share/aurorae/themes/Arc-Dark/alldesktops.svg
/usr/share/aurorae/themes/Arc-Dark/close.svg
/usr/share/aurorae/themes/Arc-Dark/decoration.svg
/usr/share/aurorae/themes/Arc-Dark/keepabove.svg
/usr/share/aurorae/themes/Arc-Dark/keepbelow.svg
/usr/share/aurorae/themes/Arc-Dark/maximize.svg
/usr/share/aurorae/themes/Arc-Dark/metadata.desktop
/usr/share/aurorae/themes/Arc-Dark/minimize.svg
/usr/share/aurorae/themes/Arc-Dark/shade.svg
```

執行

``` sh
ls -1 /usr/share/aurorae/themes
```

顯示

```
Arc
Arc-Dark
```

也就是我們可以在「/usr/share/aurorae/themes」這個資料夾

找到「Arc」和「Arc-Dark」這兩個「Aurorae Theme」。


接下來我們編輯「~/.config/kwinrc」這個檔案。

[設定片段](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kwinrc#L65-L69)如下

``` sh
[org.kde.kdecoration2]
ButtonsOnLeft=M
ButtonsOnRight=IAX
library=org.kde.kwin.aurorae
theme=__aurorae__svg__Arc-Dark
```

關於「`ButtonsOnLeft=M`」和「`ButtonsOnRight=IAX`」

可以在「Aurorae Window Decorations / [Button types](https://develop.kde.org/docs/plasma/aurorae/#button-types)」找到相關的說明。

然而「`theme=__aurorae__svg__Arc-Dark`」其中的「`Arc-Dark`」

指的就是「/usr/share/aurorae/themes/Arc-Dark」

另外「Aurorae Theme」除了可以放在「/usr/share/aurorae/themes/」這個資料夾，也就是「**系統全域**」。

也可以放在「~/.local/share/aurorae/themes」，也就是「**個人區域**」。

舉例我們可以在「GitHub」上找到「[vimix](https://github.com/vinceliuice/vimix-kde/tree/master/aurorae)」相關的「Aurorae Theme」。

放在「~/.local/share/aurorae/themes」這個資料夾。
