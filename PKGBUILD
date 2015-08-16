# Contributor: dorphell <dorphell@archlinux.org>
# Contributor: Judd Vinet <jvinet@zeroflux.org>

pkgname=lesstifextensions
pkgver=13.0.13
pkgrel=2
pkgdesc="Extensions for lesstif"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/xlt/"
license=('GPL' 'LGPL')
depends=('lesstif' 'libxpm')
makedepends=('libxaw')
options=('!libtool')
source=(http://downloads.sourceforge.net/sourceforge/xlt/Xlt-${pkgver}.tar.gz)
md5sums=('46b6259c7637d6e9b87520eb91b6ea51')

build() {
  cd ${srcdir}/Xlt-${pkgver}
  ./configure --prefix=/usr || return 1
  make || return 1
  make DESTDIR=${pkgdir} mandir=/usr/share/man htmldir=/usr/share/doc/Xlt/html install || return 1
  rm ${pkgdir}/usr/share/aclocal/ac_find_motif.m4
}
