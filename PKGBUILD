# Maintainer: panda <panda@bredos.org>

pkgname=cix-optee
pkgver=1.0.0
pkgrel=1
pkgdesc="cix optee"
arch=('aarch64')
url="https://www.bredos.org"
license=('GPL')
source=("cix-optee_0.01-1_arm64.deb")
md5sums=('bbfa315fdc4c570dd2d9e24fb261ccfd')
noextract=("${source[@]##*/}")

package() {
    ar x cix-optee_0.01-1_arm64.deb
    tar -xJf data.tar.xz
    mv $srcdir/usr $pkgdir/usr
    mv $srcdir/bin $pkgdir/usr/bin
    mv $srcdir/etc $pkgdir/etc
    mv $pkgdir/usr/sbin/* $pkgdir/usr/bin/
    rmdir $pkgdir/usr/sbin
}
