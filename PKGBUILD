# Contributor: Zsolt Udvari <udvzsolt@gmail.com>

pkgname=lua-oopango
pkgver=1.1
pkgrel=3
pkgdesc="Lua bindings to pango."
arch=(i686 x86_64)
url="http://oocairo.naquadah.org/"
license=('MIT')
depends=("lua-oocairo" "pango")
makedepends=("libtool" "pkgconfig")
source=("http://oocairo.naquadah.org/dist/oopango-${pkgver}.tar.bz2")
md5sums=(ec7a12daa387d50b570daba0a4b8aded)

build() {
  cd ${srcdir}/oopango-${pkgver}
  ./configure --prefix=/usr
  make || return 1
}

package() {
  cd ${srcdir}/oopango-${pkgver}
  make DESTDIR="$pkgdir" install
}

# vim:syntax=sh
