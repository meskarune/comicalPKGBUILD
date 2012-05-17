# Maintainer: Dolores Portalatin <meskarune@gmail.com>

pkgname=comical
pkgver=0.8
pkgrel=1
pkgdesc="Comic book reader that opens cbr and cbz archives"
arch=('i686' 'x86_64')
url="http://comical.sourceforge.net/"
license=('GPL')
groups=()
depends=('wxgtk', 'libzip')
makedepends=()
source=(http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.gz http://kambing.ui.ac.id/gentoo-portage/media-gfx/comical/files/comical-0.8-wxGTK-2.8.patch)
noextract=()
md5sums=(F5808E28FD5A2A3D21B59CDAD10ECA3D 4510063CD2ED0BA5683B6ADE771B0120)

build() {
  cd $srcdir/$pkgname-$pkgver
  patch -p1 -i $srcdir/comical-0.8-wxGTK-2.8.patch || return 1
  install -d $pkgdir/usr/local/bin/$pkgname/
  make || return 1
  cp -r $pkgdir/usr/local/bin/$pkgname/ /usr/local/bin/
  make DESTDIR=$pkgdir install || return 1
}
