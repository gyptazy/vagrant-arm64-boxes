# vagrant-arm64-boxes
<img align="left" src="https://cdn.gyptazy.ch/images/gyptazy-vagrant-boxes-arm64.jpg"/>
<br>

<p float="center"><img src="https://img.shields.io/github/issues-raw/gyptazy/vagrant-arm64-boxes"/><img alt="GitHub issues by-label" src="https://img.shields.io/github/issues/gyptazy/vagrant-arm64-boxes/bug"><img alt="GitHub issues by-label" src="https://img.shields.io/github/issues/gyptazy/vagrant-arm64-boxes/feature">
</p>


## Table of Content
- [General](#general)
- [Usage](#usage)

## General
This is the bug tracker for the collection of Vagrant Boxes for ARM64 (aarch64) based systems. This is fully compatible to Apple Silicon based Macs in combination with the VMware Fusion hypervisor as a vagrant provider. An overview of the current collection can be found on [https://gyptazy.ch/blog/collection-of-vagrant-boxes-images-for-apple-silicon-based-on-arm64/](https://gyptazy.ch/blog/collection-of-vagrant-boxes-images-for-apple-silicon-based-on-arm64/) or on the Vagrant [project](https://app.vagrantup.com/gyptazy) site.

## Usage
A short note regarding VMware Fusion (free to use for personal usage), Vagrant and the Desktop plugin of Vagrant for VMware support can be found [here](https://gyptazy.ch/notes/vagrant-virtualization-apple-silicon-mac-arm64-in-year-2023/). After choosing your desired image you just need to run on the cli the following (this example takes the FreeBSD box) commands:
```
vagrant init gyptazy/freebsd14.0-arm64
vagrant up
vagrant ssh
```

## Bugs or Box request
If you want to report a bug or have a request regarding a missing box (image), please feel free to file a bug report [here](https://github.com/gyptazy/vagrant-arm64-boxes/issues). If you have general requests for different configuration feel also free te request them.

### Known Bugs
```/sbin/ip -o -0 addr | grep -v LOOPBACK | awk '{print $2}' | sed 's/://'``` is unfortunately a known bug. However, the box (image) will still work by ssh'ing into the system by running `vagrant ssh`. This issue if already fixed in newer images. For further background information see also [here](https://github.com/gyptazy/vagrant-arm64-boxes/issues/2).