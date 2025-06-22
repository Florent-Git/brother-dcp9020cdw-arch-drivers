#!/bin/makepkg -p
# Maintainer: floshie_ <florent.ram@gmail.com>

pkgname=brother-dcp9020cdw-lpr-bin
pkgver=1.1.2
pkgrel=1
pkgdesc="LPR driver for Brother DCP-9020CDW printer"
arch=("i686" "x86_64")
url="https://support.brother.com/g/b/producttop.aspx?c=be&lang=fr&prod=dcp9020cdw_eu"
license=("EULA")
groups=("base-devel")
source=("https://download.brother.com/welcome/dlf100441/dcp9020cdwlpr-1.1.2-1.i386.deb")
md5sums=('d7fb28e4d73d56b1181833787968d0fb')

package() {
	tar -xf data.tar.gz -C "${pkgdir}"
}

