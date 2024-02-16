---
title: 設定「Lxqt」搭配「Compiz」
nav_order: 7031
has_children: false
parent: 設定「Lxqt」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Lxqt」搭配「Compiz」


## 微調腳本

| 微調腳本 |
| --- |
| [lxqt-with-compiz](https://github.com/samwhelp/lubuntu-adjustment/tree/main/prototype/main/alternative-config/lxqt-with-compiz/Main) |


## 前提

目前「Lubuntu」是採用「lxqt」這個「桌面環境」，

搭配「openbox」這個「視窗管理器」。

現在我們要來嘗試讓「lxqt」搭配「[compiz](https://samwhelp.github.io/note-about-lubuntu/read/master/window-manager/compiz.html)」。


## 操作步驟

* [安裝「Compiz」](#安裝compiz)
* [安裝「Compiz」設定檔](#安裝compiz設定檔)
* [設定「gtk-window-decorator」](#設定gtk-window-decorator)
* [設定「lxqt-session」採用「compiz」](#設定lxqt-session採用compiz)


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


``` sh
mkdir -p ~/.config/compiz-1/compizconfig

curl -fLo ~/.config/compiz-1/compizconfig/Default.ini --create-dirs https://raw.githubusercontent.com/samwhelp/lubuntu-adjustment/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/Default.ini

curl -fLo ~/.config/compiz-1/compizconfig/config --create-dirs https://raw.githubusercontent.com/samwhelp/lubuntu-adjustment/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/config

```


## 設定「gtk-window-decorator」

關於「compiz」預設採用的是「gtk-window-decorator」，

所以可以做如下的設定:

執行下面指令，設定視窗的標題列，顯示那些按鈕。

``` sh
gsettings set org.gnome.desktop.wm.preferences button-layout 'appmenu:minimize,maximize,close'
```

執行下面指令，安裝「numix-gtk-theme」

``` sh
sudo apt-get install numix-gtk-theme
```

執行下面指令，設定「gtk-window-decorator」採用「Numix」這個佈景主題。

``` sh
gsettings set org.gnome.desktop.wm.preferences theme 'Numix'
```


## 設定「lxqt-session」採用「compiz」

可以透過「圖形介面程式」來設定，

也就是透過「`lxqt-config-session` (LXQT Session Settings)」來設定。

在「Basic Settings」這個頁面，有一個選項「Window Manager」，

可以在該選項的下拉選單，選擇「compiz」，重新登出登入後，就會生效。

這個設定值，會被保存在「[~/.config/lxqt/session.conf](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-compiz/Main/asset/overlay/etc/skel/.config/lxqt/session.conf#L3)」，

所以我們也可以直接修改這個檔案，類似的設定如下

``` ini
[General]
__userfile__=true
window_manager=compiz
```

也就是「`window_manager=compiz`」那一行，修改成我們想要採用的「Window Manager」。
