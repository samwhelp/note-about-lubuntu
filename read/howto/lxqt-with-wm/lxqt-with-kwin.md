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
