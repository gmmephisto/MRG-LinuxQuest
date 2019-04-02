# Task 2

Пароль для открытия архива с образом: `MRG-LinuxQuest-Taskii-enemyunknown`

Задание:

Ты вышел на работу в компанию, к тебе пришли менеджеры и попросили найти кому отправлялись письма из Африки. Нужно построить топ-21 адресов получателей по ним. Первые буквы адресов получателей - ключ. Одно но: почтовый сервер, через который письма были отправлены не загружается.

Все ждут от вас оперативного решения вопроса!

## Step 1 - OS won't boot

* Download `CentOS` live CD and mount it to the virtual machine.
* Boot the virtual machine from live CD.
* Go to the mounted system root environment - `chroot /mnt/sysimage`.
* List logical volumes - `lvs -o vg_name,lv_name`.
* Remove non-existing logical volumes (`rd.lvm.lv=`) from GRUB defaults - `grep GRUB_CMDLINE_LINUX /etc/default/grub`.
* Recreate GRUB config file: `grub2-mkconfig -o /etc/grub2.cfg`.
* Remove non-existing logical volumes from `/etc/fstab`.

First key: `GottfriedWilhelm11646Leibniz`

## Step 2 - OS reboots immediately after boot 

* Remove `/proc/sysrq-trigger` usage from `/etc/crontab`.

Second key: `Alan1912MathisonTuring`

## Step 3 - Top email recipients from Africa

* `yum install -y epel-release`
* `yum install -y python2-geoip2`
* `pip install geoip2`
* `wget https://geolite.maxmind.com/download/geoip/database/GeoLite2-Country.tar.gz`
* `tar -xf GeoLite2-Country.tar.gz`
* `./findmail`

Third key: `LinusBenedictTorvalds`
