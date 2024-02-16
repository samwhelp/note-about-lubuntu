---
title: 設定「Lxqt」搭配「Compiz」
nav_order: 7031
has_children: false
parent: 設定「Lxqt」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Lxqt」搭配「Compiz」


## 前提

目前「Lubuntu」是採用「lxqt」這個「桌面環境」，

搭配「openbox」這個「視窗管理器」。

現在我們要來嘗試讓「lxqt」搭配「[compiz](https://samwhelp.github.io/note-about-lubuntu/read/master/window-manager/compiz.html)」。


## 操作步驟

* 安裝「Compiz」
* 安裝「Compiz」設定檔


### 安裝「Compiz」

執行下面指令，安裝「compiz」

``` sh
sudo apt-get install compiz
```

執行下面指令，安裝「compizconfig-settings-manager」

``` sh
sudo apt-get install compizconfig-settings-manager
```

執行下面指令，安裝「compiz-plugins-main」和「compiz-plugins-extra」

``` sh
sudo apt-get install compiz-plugins-main compiz-plugins-extra
```

以上可以合併在一起，執行如下


``` sh
sudo apt-get install \
	compiz \
	compizconfig-settings-manager \
	compiz-plugins-main \
	compiz-plugins-extra

```


## 安裝「Compiz」設定檔

| 關於「Compiz」設定檔路徑 |
| --- |
| [~/.config/compiz-1/compizconfig/config](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/config) |
| [~/.config/compiz-1/compizconfig/Default.ini](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/Default.ini) |
