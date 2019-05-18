
## How To Install

For Windows: Format your disk & install Linux

For Linux:
	wget -O - https://raw.githubusercontent.com/Inducido/package-manager-rosetta-stone/master/install.sh | bash

(you will be asked for sudo)


## The Rosetta Stone

| rpm                   | yum                           | debian                        | arch                              |
|-----------------------|-------------------------------|-------------------------------|-----------------------------------|
| `rpm -i foo.rpm`      |                               | `dpkg -i foo.deb`             | `pacman -U foo.pkg.tar.xz`        |
|                       | `yum install foo`             | `apt-get install foo`         | `pacman -S`                       |
| `rpm -e foo`          | `yum remove foo`              | `dpkg -P foo`                 | `pacman -R foo`                   |
| `rpm -qip foo.rpm`    |                               | `dpkg -I foo.deb`             | `pacman -Qi -p foo.pkg.tar.xz`    |
|                       | `yum info foo`                | `apt-cache show foo`          | `pacman -Si foo`                  |
| `rpm -qlp foo.rpm`    |                               | `dpkg -c foo.deb`             | `pacman -Ql -p foo.pkg.tar.xz`    |
| `rpm -ql foo`         |                               | `dpkg -L foo`                 | `pacman -Ql foo`                  |
| `rpm -qi foo`         |                               | `dpkg -p foo, dpkg -s foo`    | `pacman -Qi foo`                  |
| `rpm -q --show-scripts foo` |                         | `dpkg-query --control-list foo \| xargs -n 1 dpkg-query --control-show foo` |                        |
| `rpm -qa`             | `yum list installed`          | `dpkg-query -W, dpkg --list`  | `pacman -Q`                       |
| `rpm -qf /bin/bash`   | `yum whatprovides /bin/bash`  | `dpkg -S /bin/bash`           | `pacman -Qo /bin/bash`            |
|                       | `yum search foo`              | `apt-cache search foo`        | `pacman -Ss foo`                  |
|                       | `yum list available`          | `apt-cache dumpavail`         | `pacman -Sl`                      |
| `rpm2cpio bash.rpm \| cpio -diu` |                     | `dpkg -x bash.deb $PWD`       | `tar -xzf bash.pkg.tar.xz`        |

* http://cupcakecarnival.net/2009/02/17/debian-equivalent-rpm-based-system-commands
* http://wiki.debian.org/RPM
* https://help.ubuntu.com/community/SwitchingToUbuntu/FromLinux/RedHatEnterpriseLinuxAndFedora
* https://wiki.archlinux.org/index.php/Pacman/Rosetta_(简体中文)
* https://wiki.archlinux.org/index.php/Pacman/Rosetta
