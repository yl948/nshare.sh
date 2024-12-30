# Linux 网络共享管理工具

这是一个用于管理 Linux 系统中 SMB 和 NFS 网络共享的命令行工具。它提供了一个交互式界面，可以轻松管理网络共享的创建、挂载和删除等操作。

## 功能特点

### SMB/NFS 客户端功能
- 挂载新的 SMB/NFS 共享
  - SMB 自动扫描和手动输入
  - NFS 自动扫描和手动输入
- 查看和管理已挂载的共享
  - 显示当前挂载状态
  - 管理永久/临时挂载
  - 删除挂载点

### SMB 服务器管理
- 添加 SMB 共享
- 查看现有共享
- 删除共享
- 管理 Samba 用户

### NFS 服务器管理
- 添加 NFS 共享
- 查看现有共享
- 删除共享

## 系统要求

支持以下 Linux 发行版：
- Debian/Ubuntu
- RHEL/CentOS/Fedora
- Arch Linux

## 依赖包
- SMB 相关：
  - cifs-utils
  - smbclient
  - samba
- NFS 相关：
  - nfs-common
  - nfs-kernel-server
- 可选：
  - wsdd2 (用于改善 Windows 网络发现)

## 安装和使用

1. 方法一：直接运行（推荐）：
```bash
curl -sSL https://raw.githubusercontent.com/yl948/nshare.sh/refs/heads/main/nshare.sh | sudo bash
# 或者
wget -qO- https://raw.githubusercontent.com/yl948/nshare.sh/refs/heads/main/nshare.sh | sudo bash
```

2. 方法二：下载后运行：
```bash
wget https://raw.githubusercontent.com/yl948/nshare.sh/refs/heads/main/nshare.sh
chmod +x nshare.sh
sudo ./nshare.sh
```

## 使用说明

1. 主菜单选项：
   - SMB/NFS 功能
   - 查看/管理已挂载的共享
   - SMB 服务器共享管理
   - NFS 服务器共享管理
   - 卸载软件包

2. 创建共享：
   - 选择共享类型（SMB/NFS）
   - 设置共享路径和权限
   - 配置访问控制

3. 挂载共享：
   - 支持自动扫描和手动输入
   - 可选择永久或临时挂载
   - 自动创建挂载点

4. 管理功能：
   - 查看现有共享和挂载
   - 删除共享或取消挂载
   - 管理用户和权限

## 注意事项

1. 需要 root 权限运行
2. 建议在操作前备份重要数据
3. 永久挂载会修改 /etc/fstab 文件
4. 删除操作不可恢复，请谨慎操作
