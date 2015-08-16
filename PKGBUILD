# Maintainer: Andrea Scarpino <andrea@archlinux.org>

pkgname=kapidox
pkgver=4.99.0
pkgrel=1
pkgdesc='Frameworks API Documentation Tools'
arch=('any')
url='https://projects.kde.org/projects/frameworks/kapidox'
license=('LGPL')
depends=()
makedepends=('extra-cmake-modules' 'qt5-base' 'python')
groups=('kf5')
source=("http://download.kde.org/unstable/frameworks/${pkgver}/${pkgname}-${pkgver}.tar.xz")
md5sums=('43c0c3aad31fbb10a3039e2876eeffbf')

prepare() {
  mkdir -p build
}

build() {
  cd build
  cmake ../${pkgname}-${pkgver} \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/opt/kf5
  make
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
}
