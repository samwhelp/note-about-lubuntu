---
title: 設定「Lxqt」搭配「Xfwm4」
nav_order: 7033
has_children: false
parent: 設定「Lxqt」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Lxqt」搭配「Xfwm4」


## 微調腳本

| 微調腳本 |
| --- |
| [lxqt-with-xfwm](https://github.com/samwhelp/lubuntu-adjustment/tree/main/prototype/main/alternative-config/lxqt-with-xfwm/Main) |


## 前提

目前「Lubuntu」是採用「lxqt」這個「桌面環境」，

搭配「openbox」這個「視窗管理器」。

現在我們要來嘗試讓「lxqt」搭配「[xfwm4](https://samwhelp.github.io/note-about-lubuntu/read/master/window-manager/xfwm.html)」。


## 操作步驟

* [安裝「Xfwm4」](#安裝xfwm4)
* [關於「Xfwm4」設定檔](#關於xfwm4設定檔)
* [[設定「lxqt-session」採用「xfwm4」](#設定lxqt-session採用xfwm4)


## 安裝「Xfwm4」

執行下面指令，安裝「[xfwm4](https://packages.ubuntu.com/noble/xfwm4)」

``` sh
sudo apt-get install xfwm4
```


## 關於「Xfwm4」設定檔

| 關於「Xfwm4」設定檔路徑 |
| --- |
| [~/.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-xfwm/Main/asset/overlay/etc/skel/.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml) |
| [~/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-xfwm/Main/asset/overlay/etc/skel/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-keyboard-shortcuts.xml#L159-L234) |


## 設定「lxqt-session」採用「xfwm4」

| 設定檔路徑 |
| --- |
| [~/.config/lxqt/session.conf](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-xfwm/Main/asset/overlay/etc/skel/.config/lxqt/session.conf#L3) |


* 設定檔片段

``` ini
[General]
window_manager=xfwm4
```
