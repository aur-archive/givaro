# Contributor: Rémy Oudompheng <oudomphe@phare.normalesup.org>
# Maintainer: Antonio Rojas

pkgname=givaro
pkgver=3.8.0
pkgrel=1
pkgdesc="C++ library for arithmetic and algebraic computations"
arch=('i686' 'x86_64')
url="http://www-lmc.imag.fr/CASYS/LOGICIELS/givaro/"
license=('GPL')
depends=('gmp')
source=("https://forge.imag.fr/frs/download.php/592/$pkgname-$pkgver.tar.gz")
md5sums=('6ba1a4672a5d434d2502d17db30c86e5')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr --enable-shared 
  make
}

check() {
  cd $pkgname-$pkgver
  make check
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}

