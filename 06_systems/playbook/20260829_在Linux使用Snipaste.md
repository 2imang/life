# 20260829

## 在Linux使用Snipaste

### 下载

1. 打开[Snipaste官网](https://www.snipaste.com/)
2. 点击Download for Free下方的Download Snipaste 2 (Desktop)
3. 下载Linux安装包

### 初始工作

给.AppImage可执行权限，在文件所在文件夹打开终端

```bash
chmod +x Snipaste-*.AppImage
```

### 使用

在.AppImage所在文件夹打开终端

```bash
./Snipaste-*.AppImage --appimage-extract-and-run
```

### 卸载

**第一步：删除程序本体**
直接删除下载的 `.AppImage` 文件，以及解压出的 `squashfs-root` 文件夹（如果存在）。

**第二步：删除个人配置文件（可选，若想彻底清理）**
```bash
sudo find / -iname "*snipaste*" 2>/dev/null
rm -rf 文件
```