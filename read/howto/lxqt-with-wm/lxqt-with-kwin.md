---
title: 設定「Lxqt」搭配「Kwin」
nav_order: 7033
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
