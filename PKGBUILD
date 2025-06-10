# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Contributor: Chupligin Sergey <neochapay@gmail.com>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=qt6-quickcontrols-nemo-examples
pkgver=6.2.8
pkgrel=1
pkgdesc="Nemomobile Qt Quick Controls Examples"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/qtquickcontrols-nemo"
license=('LGPL-2.1-only AND Apache-2.0')
depends=(
    'qt6-glacier-app'
    'nemo-qml-plugin-statusnotifier'
    'qt6-quickcontrols-nemo'
)
makedepends=('cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('253c1f5008d99208e56332bde33fcd446092bb284ea5cef00777d066172bd312')

build() {
    cd "qtquickcontrols-nemo-${pkgver}"
    cmake \
        -DBUILD_EXAMPLES=ON -DBUILD_CONTROLS=OFF \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd "qtquickcontrols-nemo-${pkgver}"
    make DESTDIR="$pkgdir" install
}
