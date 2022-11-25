# OpenWrt packages feed
<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/lynxnexy/packages"> <img alt="GitHub forks" src="https://img.shields.io/github/forks/lynxnexy/packages"> <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/lynxnexy/packages"> <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/lynxnexy/packages">

## Description

This is the OpenWrt "packages"-feed containing community-maintained build scripts, options and patches for applications, modules and libraries used within OpenWrt.

Installation of pre-built packages is handled directly by the **opkg** utility within your running OpenWrt system or by using the [OpenWrt SDK](https://openwrt.org/docs/guide-developer/using_the_sdk) on a build system.

## Usage

This repository is intended to be layered on-top of an OpenWrt buildroot. If you do not have an OpenWrt buildroot installed, see the documentation at: [OpenWrt Buildroot – Installation](https://openwrt.org/docs/guide-developer/build-system/install-buildsystem) on the OpenWrt support site.

This feed is enabled by default. To install all its package definitions, run:

#### Instructions
add command
```yaml
sed -i '$a src-git lynxnexy https://github.com/lynxnexy/packages' feeds.conf.default
git pull
./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig
```
