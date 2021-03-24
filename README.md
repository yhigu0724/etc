# etc

申し込み
https://lp.kernelcare.com/iot/free-raspberry-pi-patching

返信メール１
[code]
Download KernelCare DEB package to your RPI 4 and install it:

    wget https://patches.kernelcare.com/kernelcare_2.22-1_arm64.deb20.04.deb
    export KCARE_REGISTRATION_URL=https://patches.kernelcare.com/api
    sudo -E apt install ./kernelcare_2.22-1_arm64.deb20.04.deb

After that register your RPI with a provided key and run the update:

    sudo kcarectl --register 
    sudo kcarectl --update

Your kernel is safe :)
[/code]
:---------------------------------------------------------
アップデート可能なkernel
https://patches.kernelcare.com/#All%20Kernels#

ドキュメント(日本語)
https://docs.kernelcare.com/jp/installation/

コマンドラインツール
https://docs.kernelcare.com/jp/command-line/

Ubuntuの確認
$ cat /etc/lsb-release 
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=20.04
DISTRIB_CODENAME=focal
DISTRIB_DESCRIPTION="Ubuntu 20.04.2 LTS"

$ sudo kcarectl --info
Unknown kernel (Ubuntu 5.4.0-1029-raspi), no patches available

返信メール２
[code]
Dear Ieyasu,

We are happy you decided to opt for a free KernelCare live patching for Raspberry Pi devices!
Below you will find your unique license key.

YE9UA5B627tta5JyoLwc

How to install KernelCare on Raspberry Pi 4 with Ubuntu 20.04 Focal.

Download KernelCare DEB package to your RPI 4 and install it:

    wget https://patches.kernelcare.com/kernelcare_2.22-1_arm64.deb20.04.deb
    export KCARE_REGISTRATION_URL=https://patches.kernelcare.com/api
    sudo -E apt install ./kernelcare_2.22-1_arm64.deb20.04.deb

After that register your RPI with a provided key and run the update:

    sudo kcarectl --register 
    sudo kcarectl --update

Your kernel is safe :)

Best,
The KernelCare Team
[/code]

[code]
$ sudo kcarectl --info
kpatch-state: patch is applied
kpatch-for: Linux version 5.4.0-1028-raspi (buildd@bos02-arm64-034) (gcc version 9.3.0 (Ubuntu 9.3.0-17ubuntu1~20.04)) #31-Ubuntu SMP PREEMPT Wed Jan 20 11:30:45 UTC 2021
kpatch-build-time: Thu Feb 11 23:02:52 2021
kpatch-description: 1-:1615812815;5.4.0-1028.31
[/code]
