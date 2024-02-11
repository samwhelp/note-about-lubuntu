---
title: 系統操作
nav_order: 5001
has_children: false
parent: 按鍵綁定
grand_parent: 設定
---


# 系統操作


## 重新載入設定

* [設定片段](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/share/gen/openbox-gen-rc/Section/Keybind/SystemExit.php#L34-L36)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + Shift + c`  | 重新載入設定 | `Reconfigure` (openbox 內建) |


## 登出

* [設定片段](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/share/gen/openbox-gen-rc/Section/Keybind/SystemExit.php#L24-L26)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + Shift + x`  | 登出 | `Exit` (openbox 內建) |


## 關機

* [設定片段](https://github.com/samwhelp/note-about-openbox/blob/gh-pages/_demo/config/openbox-config/main/share/gen/openbox-gen-rc/Section/Keybind/SystemExit.php#L4-L12)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Alt + Shift + z`  | Show Exit Panel | `obsession-logout` |


## 切換「顯示桌面」

* [設定片段](https://github.com/samwhelp/lubuntu-adjustment/tree/main/prototype/main/lxqt-config/Main/asset/overlay/etc/skel/.config/openbox/helper/share/gen/openbox-gen-rc/Section/Keybind/SystemToggleShowDesktop.php)

| 按鍵組合           | 功能        | 執行指令             |
| ----------------- | ------------ | -------------------- |
| `Win + d`  | 顯示「桌面操作選單」 | `ToggleShowDesktop` (openbox 內建) |

> 也可以在「桌面」使用「滑鼠左鍵」，反覆按下，就會切換「顯示桌面」。

* [設定片段](https://github.com/samwhelp/lubuntu-adjustment/tree/main/prototype/main/lxqt-config/Main/asset/overlay/etc/skel/.config/openbox/helper/share/gen/openbox-gen-rc/Section/Mousebind/Root.php#L7)
