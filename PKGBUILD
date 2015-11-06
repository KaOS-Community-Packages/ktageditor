pkgname=ktageditor
pkgver=0.2.0
pkgrel=1
pkgdesc="KTag Editor is an Audio tag editor developed in Qt5 framework."
arch=('x86_64')
url="http://karoljkocmaros.blogspot.com/p/ktag-editor.html"
license=('LGPL')
install=${pkgname}.install
makedepends=('taglib' 'phonon-qt5' 'unzip')
depends=('qt5-base>=5.1.1' 'taglib>=1.8' 'phonon-qt5')
optdepends=('phonon-qt5-vlc: audio output' 'phonon-qt5-gstreamer: audio output')
source=(${pkgname}-${pkgver}.zip::"http://master.dl.sourceforge.net/project/${pkgname}/Source/${pkgver}/${pkgname}.zip")
sha512sums=('685a34b85d057d68a9d04812e46ffe796a4a761cb7cb07fe4e0c19850cb8745e355d6e016aaee2feb35aa0f140c42e1832c2d560d20f37f94c355aea33a46f75')

build() {
    cd trunk
    qmake-qt5 PREFIX=/usr ${pkgname}.pro
    make DESTDIR="${pkgdir}"
}

package() {
    cd trunk
    make INSTALL_ROOT="${pkgdir}" install
}
