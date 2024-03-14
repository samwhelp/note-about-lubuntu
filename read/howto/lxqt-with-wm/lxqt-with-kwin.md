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
* [設定「lxqt-session」採用「kwin_x11」](#設定lxqt-session採用kwin_x11)
* [設定「Window Decoration」](#設定window-decoration)
* [設定「按鍵綁定」](#設定按鍵綁定)
* [關於「kwin-addons」](#關於kwin-addons)


## 安裝「Kwin」

執行下面指令，安裝「[kwin-x11](https://packages.ubuntu.com/noble/kwin-x11)」

``` sh
sudo apt-get install kwin-x11
```

因為我們會使用到一些「Kwin Plugin」，所以執行下面指令，安裝「[kwin-addons](https://packages.ubuntu.com/noble/kwin-addons)」。

``` sh
sudo apt-get install kwin-addons
```

以上可以合併在一起，執行如下

``` sh
sudo apt-get install \
	kwin-x11 \
	kwin-addons

```

> 關於我們用到那些「Kwin Plugin」，會在下面『[關於「kwin-addons」](#關於kwin-addons)』解說。


## 關於「Kwin」設定檔

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
| [~/.config/krunnerrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/krunnerrc) |
| [~/.config/ktimezonedrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/ktimezonedrc) |


## 設定「lxqt-session」採用「kwin_x11」

| 設定檔路徑 |
| --- |
| [~/.config/lxqt/session.conf](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/lxqt/session.conf#L3) |


* 設定檔片段

``` ini
[General]
window_manager=kwin_x11
```


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

複製「[/usr/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/sample/orginal/screengrab.desktop)」到「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」，

編輯「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」，加入一些「Action」如下


* [FullScreenScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L99-L158)
* [ActiveWindowScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L168-L219)
* [RectangularRegionScreenShot](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop#L221-L288)


架構上的「設定片段」修改如下，完整的請對照我修改過後的「[~/.local/share/applications/screengrab.desktop](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.local/share/applications/screengrab.desktop)」。

``` ini
[Desktop Entry]
Name=ScreenGrab
Exec=screengrab
X-KDE-Shortcuts=Alt+Print
Actions=FullScreenScreenShot;ActiveWindowScreenShot;RectangularRegionScreenShot;

[Desktop Action FullScreenScreenShot]
Name=Capture Entire Desktop
Exec=screengrab --fullscreen
X-KDE-Shortcuts=Print

[Desktop Action ActiveWindowScreenShot]
Name=Capture Active Window
Exec=screengrab --active
X-KDE-Shortcuts=Meta+Print

[Desktop Action RectangularRegionScreenShot]
Name=Capture Rectangular Region
Exec=screengrab --region
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

然而「第一個欄位」才是「按鍵綁定設定值」，設定成「`none`」則是停用「預設的按鍵綁定」。

最後「第三個欄位」則是「顯示名稱」。


| Action                          | 第一個欄位          | 第二個欄位          | 第三個欄位                  |
| ------------------------------- | ------------------- | ------------------- | --------------------------- |
| **執行動作**                    | **按鍵綁定設定值**  | **預設的按鍵綁定**  | **顯示名稱**                |
| `_launch=`                      | `Alt+Print`         | `Alt+Print`         | ScreenGrab                  |
| `FullScreenScreenShot=`         | `Print`             | `Print`             | Capture Entire Desktop      |
| `ActiveWindowScreenShot=`       | `Meta+Print`        | `Meta+Print`        | Capture Active Window       |
| `RectangularRegionScreenShot=`  | `Ctrl+Print`        | `Ctrl+Print`        | Capture Rectangular Region  |


## 關於「kwin-addons」

上面有提到，因為我們會使用到一些「Kwin Plugin」，所以安裝了「[kwin-addons](https://packages.ubuntu.com/noble/amd64/kwin-addons)」。

在還沒有安裝「kwin-addons」之前，

當啟動了「KDE System Settings」後，

在「Window Management / Task Switcher」這個頁面，

有兩個頁籤「Main」和「Alternative」，

在「Visualization」有一個下拉選單，選項如下

* 「Breeze」

在安裝「kwin-addons」之後，下拉選單，選項會變成如下

* 「Breeze」
* 「Compact」
* 「Cover Switch」
* 「Flip Switch」
* 「Grid」
* 「Informative」
* 「Large Icons」
* 「Small Icons」
* 「Text Only」
* 「Thumbnail Grid」
* 「Thumbnails」

可以執行「`grep '"Name"' /usr/share/kwin/tabbox/*/*.json`」找到上面列出的「Name」。

* Ubuntu Package / kwin-addons / [filelist](https://packages.ubuntu.com/noble/amd64/kwin-addons/filelist)

執行

``` sh
dpkg -L kwin-addons
```

顯示

```
/.
/usr
/usr/share
/usr/share/doc
/usr/share/doc/kwin-addons
/usr/share/doc/kwin-addons/changelog.Debian.gz
/usr/share/doc/kwin-addons/copyright
/usr/share/kwin
/usr/share/kwin/desktoptabbox
/usr/share/kwin/desktoptabbox/previews
/usr/share/kwin/desktoptabbox/previews/contents
/usr/share/kwin/desktoptabbox/previews/contents/ui
/usr/share/kwin/desktoptabbox/previews/contents/ui/main.qml
/usr/share/kwin/desktoptabbox/previews/metadata.json
/usr/share/kwin/tabbox
/usr/share/kwin/tabbox/big_icons
/usr/share/kwin/tabbox/big_icons/contents
/usr/share/kwin/tabbox/big_icons/contents/ui
/usr/share/kwin/tabbox/big_icons/contents/ui/IconTabBox.qml
/usr/share/kwin/tabbox/big_icons/contents/ui/main.qml
/usr/share/kwin/tabbox/big_icons/metadata.json
/usr/share/kwin/tabbox/compact
/usr/share/kwin/tabbox/compact/contents
/usr/share/kwin/tabbox/compact/contents/ui
/usr/share/kwin/tabbox/compact/contents/ui/main.qml
/usr/share/kwin/tabbox/compact/metadata.json
/usr/share/kwin/tabbox/coverswitch
/usr/share/kwin/tabbox/coverswitch/contents
/usr/share/kwin/tabbox/coverswitch/contents/ui
/usr/share/kwin/tabbox/coverswitch/contents/ui/main.qml
/usr/share/kwin/tabbox/coverswitch/metadata.json
/usr/share/kwin/tabbox/flipswitch
/usr/share/kwin/tabbox/flipswitch/contents
/usr/share/kwin/tabbox/flipswitch/contents/ui
/usr/share/kwin/tabbox/flipswitch/contents/ui/main.qml
/usr/share/kwin/tabbox/flipswitch/metadata.json
/usr/share/kwin/tabbox/informative
/usr/share/kwin/tabbox/informative/contents
/usr/share/kwin/tabbox/informative/contents/ui
/usr/share/kwin/tabbox/informative/contents/ui/main.qml
/usr/share/kwin/tabbox/informative/metadata.json
/usr/share/kwin/tabbox/present_windows
/usr/share/kwin/tabbox/present_windows/contents
/usr/share/kwin/tabbox/present_windows/contents/ui
/usr/share/kwin/tabbox/present_windows/contents/ui/main.qml
/usr/share/kwin/tabbox/present_windows/metadata.json
/usr/share/kwin/tabbox/small_icons
/usr/share/kwin/tabbox/small_icons/contents
/usr/share/kwin/tabbox/small_icons/contents/ui
/usr/share/kwin/tabbox/small_icons/contents/ui/IconTabBox.qml
/usr/share/kwin/tabbox/small_icons/contents/ui/main.qml
/usr/share/kwin/tabbox/small_icons/metadata.json
/usr/share/kwin/tabbox/text
/usr/share/kwin/tabbox/text/contents
/usr/share/kwin/tabbox/text/contents/ui
/usr/share/kwin/tabbox/text/contents/ui/main.qml
/usr/share/kwin/tabbox/text/metadata.json
/usr/share/kwin/tabbox/thumbnail_grid
/usr/share/kwin/tabbox/thumbnail_grid/contents
/usr/share/kwin/tabbox/thumbnail_grid/contents/ui
/usr/share/kwin/tabbox/thumbnail_grid/contents/ui/main.qml
/usr/share/kwin/tabbox/thumbnail_grid/metadata.json
/usr/share/kwin/tabbox/thumbnails
/usr/share/kwin/tabbox/thumbnails/contents
/usr/share/kwin/tabbox/thumbnails/contents/ui
/usr/share/kwin/tabbox/thumbnails/contents/ui/main.qml
/usr/share/kwin/tabbox/thumbnails/metadata.json
```

我們在「Window Management / Task Switcher / **Main** / Visualization」下拉選單，選的是「**Large Icons**」

會被紀錄在「[~/.config/kwinrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kwinrc#L55-L56)」，「設定片段」如下

``` ini
[TabBox]
LayoutName=big_icons
```

我們在「Window Management / Task Switcher / **Alternative** / Visualization」下拉選單，選的是「**Cover Switch**」

會被紀錄在「[~/.config/kwinrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kwinrc#L58-L59)」，「設定片段」如下

``` ini
[TabBoxAlternative]
LayoutName=coverswitch
```


執行「`grep '"Id"' /usr/share/kwin/tabbox/*/*.json`」可以找到「Id」。

執行「`grep '"Name"' /usr/share/kwin/tabbox/*/*.json`」可以找到「Name」。


| Name              | Id                 |
| ----------------- | ------------------ |
| `Compact`         | `compact`          |
| `Cover Switch`    | `coverswitch`      |
| `Flip Switch`     | `flipswitch`       |
| `Grid`            | `present_windows`  |
| `Informative`     | `informative`      |
| `Large Icons`     | `big_icons`        |
| `Small Icons`     | `small_icons`      |
| `Text Only`       | `text`             |
| `Thumbnail Grid`  | `thumbnail_grid`   |
| `Thumbnails`      | `thumbnails`       |


我們在「Window Management / Task Switcher / **Main** / Shortcuts / All Windows」

* 在「Forward」設定的是「`Meta + S`」，也就是按鍵綁定「`Win + s`」。
* 在「Reverse」設定的是「`Meta + A`」，也就是按鍵綁定「`Win + a`」。

會被紀錄在「[~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L123-L124)」，「設定片段」如下

```
Walk Through Windows=Meta+S,Alt+Tab,Walk Through Windows
Walk Through Windows (Reverse)=Meta+A,Alt+Shift+Backtab,Walk Through Windows (Reverse)
```

我們在「Window Management / Task Switcher / **Alternative** / Shortcuts / All Windows」

* 在「Forward」設定的是「`Meta + Esc`」，也就是按鍵綁定「`Win + Esc`」。
* 在「Reverse」設定的是「`Alt + Esc`」，也就是按鍵綁定「`Alt + Esc`」。

會被紀錄在「[~/.config/kglobalshortcutsrc](https://github.com/samwhelp/lubuntu-adjustment/blob/main/prototype/main/alternative-config/lxqt-with-kwin/Main/asset/overlay/etc/skel/.config/kglobalshortcutsrc#L125-L126)」，「設定片段」如下

```
Walk Through Windows Alternative=Meta+Esc,,Walk Through Windows Alternative
Walk Through Windows Alternative (Reverse)=Alt+Esc,,Walk Through Windows Alternative (Reverse)
```


關於「KDE System Settings / Window Management / Task Switcher」這個頁面。

執行

``` sh
grep '^Exec=' /usr/share/applications/kcm_kwintabbox.desktop
```

顯示

```
Exec=systemsettings kcm_kwintabbox
```

所以直接執行下面指令

``` sh
systemsettings kcm_kwintabbox
```

當啟動了「KDE System Settings」後，

就會直接切換到「Window Management / Task Switcher」這個頁面。
