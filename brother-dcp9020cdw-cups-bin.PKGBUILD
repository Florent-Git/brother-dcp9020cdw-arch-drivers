#!/bin/makepkg -p
# Maintainer: floshie_ <florent.ram@gmail.com>

pkgname=brother-dcp9020cdw-cups-bin
_printer=dcp9020cdw
pkgver=1.1.4
pkgrel=1
pkgdesc="CUPS wrapper for Brother DCP-9020CDW printer"
arch=("i686" "x86_64")
url="https://support.brother.com/g/b/producttop.aspx?c=be&lang=fr&prod=dcp9020cdw_eu"
license=("EULA")
groups=("base-devel")
source=("https://download.brother.com/welcome/dlf100443/dcp9020cdwcupswrapper-1.1.4-0.i386.deb")
md5sums=('8283e3ca2d8e8873f852ed2321483fdc')

package() {
    tar -xf data.tar.gz -C "$pkgdir"

    cd "$pkgdir"

    install -Dm644 "opt/brother/Printers/$_printer/cupswrapper/brother_${_printer}_printer_en.ppd" \
        -t "usr/share/cups/model/Brother"

    install -Dm644 "opt/brother/Printers/$_printer/cupswrapper/brother_${_printer}_printer_en.ppd" \
        -t "usr/share/ppd/Brother"

    mkdir -p -m755 "$pkgdir/usr/lib/cups/filter"
    ln -s "/opt/brother/Printers/$_printer/cupswrapper/brother_lpdwrapper_$_printer" \
        "usr/lib/cups/filter"

}

