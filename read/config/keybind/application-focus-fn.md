---
title: 聚焦應用程式 (常用的)
nav_order: 5014
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 聚焦應用程式 (常用的)


* $ man [wmctrl](http://manpages.ubuntu.com/manpages/jammy/en/man1/wmctrl.1.html)
* [openbox-focus-ctrl](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/bin/openbox-focus-ctrl)
* [設定片段](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/share/gen/openbox-gen-rc/Section/Keybind/ApplicationFocusFn.php#L3-L26)


| 按鍵組合          | 功能           | 執行指令     |
| ----------------- | -------------- | ------------ |
| `Win + F1` | 開啟或聚焦檔案管理器 | `pcmanfm-qt` 或是 `wmctrl -x -a pcmanfm-qt` |
| `Win + F2` | 開啟或聚焦文字編輯器 | `atom` 或是 `wmctrl -x -a atom`     |
| `Win + F3` | 開啟或聚焦啟網頁瀏覽器 | `firefox` 或是 `wmctrl -x -a firefox`   |
| `Win + F4` | 開啟或聚焦終端機    | `sakura` 或是 `wmctrl -x -a sakura`    |


* [設定片段](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/share/gen/openbox-gen-rc/Section/Keybind/ApplicationFocusFn.php#L31-L54)


| 按鍵組合          | 功能           | 執行指令     |
| ----------------- | -------------- | ------------ |
| `Shift + F1` | 開啟或聚焦檔案管理器 | `thunar` 或是 `wmctrl -x -a thunar` |
| `Shift + F2` | 開啟或聚焦文字編輯器 | `mousepad` 或是 `wmctrl -x -a mousepad`     |
| `Shift + F3` | 開啟或聚焦網頁瀏覽器 | `firefox` 或是 `wmctrl -x -a firefox`   |
| `Shift + F4` | 開啟或聚焦終端機    | `xfce4-terminal` 或是 `wmctrl -x -a xfce4-terminal`    |
