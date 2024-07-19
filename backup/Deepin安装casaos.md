# Deepin系统安装casaos

## 一般在深度deepin系统下是无法使用CasaOS的会报错

​![image](https://raw.githubusercontent.com/saltedfishjun/photo/main/picgo/20240608124003.png)​

# 打补丁（安装2个依赖包）

### 安装深度deepin缺少的依赖包udevil

```1c
wget https://mirrors-i.tuna.tsinghua.edu.cn/debian/pool/main/u/udevil/udevil_0.4.4-3_amd64.deb
sudo dpkg -i udevil_0.4.4-3_amd64.deb
```

### 安装深度deepin缺少的依赖包mergerfs

```1c
wget https://mirrors.sohu.com/deepin/pool/main/m/mergerfs/mergerfs_2.24.2-4_amd64.deb
sudo dpkg -i mergerfs_2.24.2-4_amd64.deb
```

由于CasaOS暂时没有适配深度deepin v23系统,但适配了标准的Debian 12。

而深度deepin系统恰好是基于debian 12制作的，嘿，那就先伪装一下debian 12/bookworm

从而让CasaOS的脚本顺利通过。

暂时修改一下/etc/os-release 中的ID和VERSION_CODENAME

### 备份一下配置文件

**备份一下原始文件**

```1c
sudo cp /etc/os-release /etc/os-release.backup
```

#### 修改系统名称和代号，待CasaOS安装成功后，还原回来。

```1c
sudo sed -i -e 's/^ID=.*$/ID=debian/' -e 's/^VERSION_CODENAME=.*$/VERSION_CODENAME=bookworm/' /etc/os-release
```

### 在深度deepin v20（debian 12） 系统下安装CasaOS

```1c
curl -fsSL https://get.casaos.io | sudo bash
```

### 安装成功后,记得将系统名称还原回来

**CasaOS安装成功之后,要记得还原配置文件**

```1c
sudo mv /etc/os-release.backup /etc/os-release
```