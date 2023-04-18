在按照基础环境篇安装完成后，下一步就是安装桌面环境了。
# 安装窗口图形系统
窗口图形系统有两种选择—— Xorg 和 Wayland。
**虽然可以使用 Wayland 启动 KDE Plasma，但仍存在一些缺失的功能和已知问题。建议使用 Xorg 以获得最完整和稳定的体验。**

执行下面命令安装 Xorg 的一些组件：
```bash
sudo pacman -S xorg-server xorg-apps xorg-xinit xorg-xclock xterm
```
安装完成后，可执行 ```startx```测试 Xorg 是否正常工作。
（执行```exit```退出 Xorg 测试界面）

# 安装 KDE Plasma
执行下面命令安装 KDE Plasma：
```bash
sudo pacman -S plasma
```
如果你想一次性安装全部 KDE 应用，可执行下面命令（可选）：
```bash
sudo pacman -S kde-applications
```
下面是安装个人喜欢的一些 KDE 应用，执行
```bash
sudo pacman -S dolphin konsole kate kdeconnect ark gwenview partitionmanager filelight kcalc kdenlive krita kdiskmark
```
（KDE 应用详见 https://apps.kde.org/zh-cn/）

## 启用登录管理器
启用 SDDM，进入桌面环境：
```bash
sudo systemctl enable --now sddm
```

## 浏览器及字体渲染
进入桌面环境后，按 Ctrl+Alt+T 可打开终端。
执行下面命令安装 Firefox：
```bash
sudo pacman -S firefox
```
常用的中文字体有以下这些：

- wqy-microhei
- wqy-microhei-lite
- wqy-bitmapfont
- wqy-zenhei
- ttf-arphic-ukai
- ttf-arphic-uming
- ttf-sarasa-gothic
- adobe-source-han-sans-cn-fonts
- adobe-source-han-serif-cn-fonts
- noto-fonts-cjk

使用
```bash
sudo pacman -S 字体名
```
安装。
一次性安装上述全部字体：
```bash
sudo pacman -S wqy-microhei wqy-microhei-lite wqy-bitmapfont wqy-zenhei ttf-arphic-ukai ttf-arphic-uming ttf-sarasa-gothic adobe-source-han-sans-cn-fonts adobe-source-han-serif-cn-fonts noto-fonts-cjk
```
（未完待续）
