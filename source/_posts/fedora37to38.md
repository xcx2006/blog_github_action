---
title: fedora更新 悲
date: 2023-04-29 14:59:53
comment: true
tags:
    - "linux"
    - "fedora"
    - "翻车"
categories:
    - "linux"
excerpt: "=("
---
```
[xuchengxi@fedora 下载]$ sudo dnf system-upgrade download --releasever=38
[sudo] xuchengxi 的密码：Before you continue ensure that your system is fully upgraded by running "dnf --refresh upgrade". Do you want to continue [y/N]: y
Copr repo for onedriver owned by jstaf                                        245  B/s | 3.3 kB     00:13    
Fedora 38 - x86_64                                                            1.7 kB/s | 5.6 kB     00:03    
Fedora 38 - x86_64 - Debug                                                    471  B/s | 4.6 kB     00:10    
Fedora 38 - Source                                                            2.9 kB/s | 5.3 kB     00:01    
Fedora 38 openh264 (From Cisco) - x86_64                                      300  B/s | 989  B     00:03    
Fedora 38 openh264 (From Cisco) - x86_64 - Debug                              595  B/s | 997  B     00:01    
Fedora Modular 38 - x86_64                                                    1.0 kB/s | 5.5 kB     00:05    
Fedora Modular 38 - x86_64 - Debug                                            934  B/s | 4.6 kB     00:05    
Fedora Modular 38 - Source                                                    913  B/s | 5.2 kB     00:05    
Fedora 38 - x86_64 - Updates                                                   11 kB/s | 6.0 kB     00:00    
Fedora 38 - x86_64 - Updates                                                  152 kB/s | 500 kB     00:03    
Fedora 38 - x86_64 - Updates - Debug                                          9.9 kB/s | 5.3 kB     00:00    
Fedora 38 - x86_64 - Updates - Debug                                          3.2 kB/s | 4.9 kB     00:01    
Fedora 38 - Updates Source                                                     15 kB/s | 5.8 kB     00:00    
Fedora 38 - Updates Source                                                    1.6 kB/s | 5.9 kB     00:03    
Fedora Modular 38 - x86_64 - Updates                                          1.1 kB/s | 5.4 kB     00:04    
Fedora Modular 38 - x86_64 - Updates - Debug                                  8.6 kB/s | 4.4 kB     00:00    
Fedora Modular 38 - Updates Source                                            5.7 kB/s | 5.2 kB     00:00    
FZUG fc38 - Free                                                              8.6 kB/s | 3.0 kB     00:00    
FZUG fc38 - Nonfree                                                            11 kB/s | 3.0 kB     00:00    
google-chrome                                                                 2.5 kB/s | 1.3 kB     00:00    
microsoft-edge                                                                1.9 kB/s | 1.5 kB     00:00    
RPM Fusion for Fedora 38 - Free                                               1.0 kB/s |  11 kB     00:10    
RPM Fusion for Fedora 38 - Free - Updates                                     586  B/s | 9.5 kB     00:16    
RPM Fusion for Fedora 38 - Nonfree                                            3.0 kB/s |  15 kB     00:04    
RPM Fusion for Fedora 38 - Nonfree - Updates                                  7.7 kB/s |  13 kB     00:01    
WineHQ packages                                                               2.1 kB/s | 3.0 kB     00:01    
没有和组 "gimp-heif-plugin" 匹配的没有和组 "hanazono-fonts" 匹配的没有和组 "vlgothic-p-fonts" 匹配的没有和组 "google-noto-looped-lao-ui-vf-fonts" 匹配的没有和组 "google-noto-sans-myanmar-ui-vf-fonts" 匹配的没有和组 "scim-bridge-gtk" 匹配的没有和组 "drehatlas-warender-bibliothek-fonts" 匹配的没有和组 "google-noto-serif-nyiakeng-puachue-hmong-vf-fonts" 匹配的没有和组 "google-noto-sans-oriya-ui-vf-fonts" 匹配的没有和组 "sil-scheherazade-fonts" 匹配的没有和组 "google-noto-sans-kannada-ui-vf-fonts" 匹配的没有和组 "vlgothic-fonts" 匹配的没有和组 "google-noto-sans-malayalam-ui-vf-fonts" 匹配的没有和组 "google-noto-sans-khmer-ui-vf-fonts" 匹配的没有和组 "google-noto-sans-telugu-ui-vf-fonts" 匹配的没有和组 "google-noto-looped-thai-ui-vf-fonts" 匹配的没有和组 "google-noto-sans-sinhala-ui-vf-fonts" 匹配的没有和组 "drehatlas-xaporho-fonts" 匹配的没有和组 "google-noto-sans-thai-ui-vf-fonts" 匹配的没有和组 "google-noto-serif-tamil-slanted-vf-fonts" 匹配的没有和组 "ipa-ex-gothic-fonts" 匹配的没有和组 "yanone-tagesschrift-fonts" 匹配的没有和组 "google-noto-sans-tamil-ui-vf-fonts" 匹配的没有和组 "google-noto-serif-dogra-vf-fonts" 匹配的没有和组 "reiserfs-utils" 匹配的没有和组 "tlomt-junction-fonts" 匹配的没有和组 "cups-bjnp" 匹配的没有和组 "scim-anthy" 匹配的没有和组 "google-noto-sans-hebrew-droid-vf-fonts" 匹配的没有和组 "ht-caladea-fonts" 匹配的没有和组 "ubuntu-title-fonts" 匹配的没有和组 "authselect-compat" 匹配的没有和组 "google-noto-looped-thai-vf-fonts" 匹配的没有和组 "culmus-shofar-fonts" 匹配的没有和组 "vollkorn-fonts" 匹配的没有和组 "google-noto-sans-lao-ui-vf-fonts" 匹配的没有和组 "google-noto-looped-lao-vf-fonts" 匹配的没有和组 "google-noto-sans-hebrew-new-vf-fonts" 匹配的没有和组 "google-noto-sans-bengali-ui-vf-fonts" 匹配的没有和组 "google-noto-kufi-arabic-vf-fonts" 匹配的没有和组 "google-noto-sans-tai-viet-vf-fonts" 匹配的没有和组 "cave9-mutante-fonts" 匹配的没有和组 "imsettings-systemd" 匹配的没有和组 "google-noto-sans-display-vf-fonts" 匹配的没有和组 "plasma-workspace-xorg" 匹配的没有和组 "google-noto-sans-gurmukhi-ui-vf-fonts" 匹配的没有和组 "google-noto-serif-display-vf-fonts" 匹配的没有和组 "google-noto-sans-zanabazar-square-vf-fonts" 匹配的没有和组 "scim-bridge-qt3" 匹配的没有和组 "scim-bridge-qt" 匹配的没有和组 "google-noto-sans-arabic-ui-vf-fonts" 匹配的没有和组 "google-noto-sans-tamil-supplement-vf-fonts" 匹配的没有和组 "google-noto-sans-runic-vf-fonts" 匹配的没有和组 "polarsys-b612-sans-fonts" 匹配的没有和组 "ipa-ex-mincho-fonts" 匹配的没有和组 "kanjistrokeorders-fonts" 匹配的错误： 问题 1: 安装的软件包的问题 iptables-nft-1.8.8-4.fc37.x86_64
  - 软件包 kernel-lt-5.4.228-1.el7.elrepo.x86_64 与 iptables < 1.3.2-1（由 iptables-nft-1.8.9-2.fc38.x86_64 提供）冲突  - iptables-nft-1.8.8-4.fc37.x86_64 不属于 distupgrade 仓库  - 安装的软件包的问题 kernel-lt-5.4.228-1.el7.elrepo.x86_64
 问题 2: 安装的软件包的问题 libswscale-free-5.1.3-1.fc37.x86_64
  - 软件包 ffmpeg-libs-6.0-6.fc38.x86_64 与 libswscale-free（由 libswscale-free-6.0-2.fc38.x86_64 提供）冲突  - 软件包 ffmpeg-libs-6.0-6.fc38.x86_64 与 libswscale-free（由 libswscale-free-6.0-4.fc38.x86_64 提供）冲突  - 软件包 ffmpeg-6.0-6.fc38.x86_64 需要 ffmpeg-libs(x86-64) = 6.0-6.fc38，但没有提供者可以被安装  - libswscale-free-5.1.3-1.fc37.x86_64 不属于 distupgrade 仓库  - 冲突的请求
```
