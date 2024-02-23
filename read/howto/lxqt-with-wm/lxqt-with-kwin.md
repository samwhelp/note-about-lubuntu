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
* [設定「按鍵綁定」](#設定按鍵綁定)


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

另外「Aurorae Theme」放置的資料夾，

除了可以放在「/usr/share/aurorae/themes/」這個資料夾，也就是「**系統全域**」。

也可以放在「~/.local/share/aurorae/themes」，也就是「**個人區域**」。

舉例我們可以在「GitHub」上找到「[vimix](https://github.com/vinceliuice/vimix-kde/tree/master/aurorae)」相關的「Aurorae Theme」。

放在「~/.local/share/aurorae/themes」這個資料夾。


## 設定「按鍵綁定」

我是拿我之前在「Kde Plasma」的「[按鍵綁定](https://samwhelp.github.io/note-about-kde/read/config/keybind.html#%E8%A8%AD%E5%AE%9A%E6%AA%94)」來做修改，

也就是使用「圖形介面程式 (shortcut)」搭配編輯「[~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc)」這個檔案。

大致上，主軸的「[按鍵綁定](https://samwhelp.github.io/note-about-kde/read/config/keybind.html)」是相同的，

只是做一些細微的調整，符合「lxqt」的操作。

例如

| 按鍵組合 | 功能 | 執行指令 |
| -------- | ---- | -------- |
| `Alt + Shift + x` | [Logout](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L209-L211) | `lxqt-leave --logout` |
| `Alt + Shift + z` | [Leave](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L205-L207) | `lxqt-leave` |


### 「螢幕截圖」的「按鍵綁定」

原本在「KDE Plasma」採用的「[螢幕截圖程式](https://samwhelp.github.io/note-about-kde/read/config/keybind/screenshot-control)」是「[Spectacle](https://apps.kde.org/spectacle/)」。

我們要改成在「Lxqt」環境所採用的「ScreenGrab」。

所以要調整「Kwin」的「[按鍵綁定](https://samwhelp.github.io/note-about-lubuntu/read/config/keybind/screenshot)」。

| 按鍵組合        | 功能                  | 執行指令                   |
| --------------- | --------------------- | -------------------------- |
| `Print`         | 整個桌面螢幕截圖      | `screengrab --fullscreen`  |
| `Alt + Print`   | 啟動螢幕截圖程式      | `screengrab`               |
| `Win + Print`   | 目前視窗截圖          | `screengrab --active`      |
| `Ctrl + Print`  | 選取螢幕畫面區塊截圖  | `screengrab --region`      |


仿照「[/usr/share/applications/org.kde.spectacle.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/sample/orginal/org.kde.spectacle.desktop)」的作法。

複製「[/usr/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/sample/orginal/screengrab.desktop)」到「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」

編輯「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」，加入一些「Action」如下


* [FullScreenScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L99-L158)
* [ActiveWindowScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L168-L219)
* [RectangularRegionScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L221-L288)


架構上的「設定片段」修改如下，完整的請對照我修改過後的「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」。

``` ini
[Desktop Entry]
X-KDE-Shortcuts=Alt+Print
Actions=FullScreenScreenShot;ActiveWindowScreenShot;RectangularRegionScreenShot;

[Desktop Action FullScreenScreenShot]
X-KDE-Shortcuts=Print

[Desktop Action ActiveWindowScreenShot]
X-KDE-Shortcuts=Meta+Print

[Desktop Action RectangularRegionScreenShot]
X-KDE-Shortcuts=Ctrl+Print
```

要注意的是在「`[Desktop Entry]`」這個區塊，

要設定「`Actions=FullScreenScreenShot;ActiveWindowScreenShot;RectangularRegionScreenShot;`」，

也就是「Action」的列表。

而「`X-KDE-Shortcuts=`」的作用，

就是使用「圖形介面程式 (shortcut)」操作時，

加入「ScreenGrab」這個「Application」，

就會產生預設的「按鍵綁定」。

也就是會在「[~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L323-L328)」這個檔案，加入如下的設定片段

``` ini
[screengrab.desktop]
ActiveWindowScreenShot=Meta+Print,Meta+Print,Capture Active Window
FullScreenScreenShot=Print,Print,Capture Entire Desktop
RectangularRegionScreenShot=Ctrl+Print,Ctrl+Print,Capture Rectangular Region
_k_friendly_name=ScreenGrab
_launch=Alt+Print,Alt+Print,ScreenGrab
```

**注意**:「預設的按鍵綁定」是在「第二個欄位」，

然而「第一個欄位」才是「按鍵綁定設定值」，設定成「none」則是停用「預設的按鍵綁定」。

最後「第三個欄位」則是「顯示名稱」。


| Action                          | 第一個欄位          | 第二個欄位          | 第三個欄位                  |
| ------------------------------- | ------------------- | ------------------- | --------------------------- |
| **執行動作**                    | **按鍵綁定設定值**  | **預設的按鍵綁定**  | **顯示名稱**                |
| `_launch=`                      | `Alt+Print`         | `Alt+Print`         | ScreenGrab                  |
| `FullScreenScreenShot=`         | `Print`             | `Print`             | Capture Entire Desktop      |
| `ActiveWindowScreenShot=`       | `Meta+Print`        | `Meta+Print`        | Capture Active Window       |
| `RectangularRegionScreenShot=`  | `Ctrl+Print`        | `Ctrl+Print`        | Capture Rectangular Region  |
