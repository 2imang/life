# 20260904

## Ubuntu切换至nvidia驱动

### 问题描述

在尝试使用 whisper 时，发现默认调用设备是cpu，尝试调用gpu，发现无法使用 cuda

可能是自己的显卡驱动没装好

出现以下情况

```bash
nvidia-smi
NVIDIA-SMI has failed because it couldn't communicate with the NVIDIA driver. Make sure that the latest NVIDIA driver is installed and running.
```

### 解决方法

查了一些资料，可能是已有驱动版本和内核版本不匹配，需要更新驱动版本

查看内核版本
```bash
uname -r
6.8.0-138-generic
```

查看驱动版本
```bash
apt list --installed | grep -i nvidia
```

```bash
sudo ubuntu-driver install
```

安装后重启即可检测到驱动，正常使用cuda

```bash
reboot
```
