---
title: "Install"
description: "a2fa Installation"
---

a2fa is a command line tool for generating and validating one-time password. Its purpose is to get rid of phones and be able to authenticate easily. It keeps synced with Google Authenticator, Microsoft Authenticator.

# Install

## Linux installation

### Script installation

One-liner bash script to install a2fa

    sudo -v ; curl https://raw.githubusercontent.com/csyezheng/a2fa/main/scripts/install.sh | sudo bash

### Manual installation

Fetch and unpack

    curl -LO "https://github.com/csyezheng/a2fa/releases/latest/download/a2fa_Linux_x86_64.tar.gz"
    mkdir /tmp/a2fa
    tar -xzf a2fa_Linux_x86_64.tar.gz -C /tmp/a2fa

Copy binary file

    sudo cp /tmp/a2fa/a2fa /usr/bin/
    sudo chown root:root /usr/bin/a2fa
    sudo chmod 755 /usr/bin/a2fa

clean files

```
rm -r /tmp/a2fa
rm a2fa_Linux_x86_64.tar.gz
```

## macOS installation

### Script installation

One-liner bash script to install a2fa

    sudo -v ; curl https://raw.githubusercontent.com/csyezheng/a2fa/main/scripts/install.sh | sudo bash

### Manual installation

Fetch and unpack

    curl -LO https://github.com/csyezheng/a2fa/releases/latest/download/a2fa_Darwin_x86_64.tar.gz
    mkdir /tmp/a2fa
    tar -xzf a2fa_Linux_x86_64.tar.gz -C /tmp/a2fa

Copy binary file

    sudo mkdir -m 0555 /usr/local/bin
    sudo cp /tmp/a2fa/a2fa /usr/local/bin/a2fa.new
    sudo mv /usr/local/bin/a2fa.new /usr/local/bin/a2fa
    sudo chmod a=x /usr/bin/a2fa

Remove the leftover files.

    rm -r /tmp/a2fa/a2fa 
    rm a2fa_Darwin_x86_64.tar.gz

## Windows installation

### Script installation

One-liner PowerShell script to install a2fa

```
Invoke-Expression "& { $(Invoke-RestMethod 'https://raw.githubusercontent.com/csyezheng/a2fa/main/scripts/install.ps1') }"
```
### Manual installation

Download precompiled binary from [release](https://github.com/csyezheng/a2fa/releases/) page. Open this file in the Explorer and extract `a2fa.exe`. a2fa is a portable executable so you can place it wherever is convenient. Open a CMD window (or powershell) and run the binary.



