# Maintainer: Joren Van Onder <joren.vanonder@gmail.com>
pkgname=plover-git
_gitname=plover
pkgver=v2.5.8
pkgrel=1
pkgdesc="A free, open source program providing realtime stenographic technology."
arch=(any)
url="https://github.com/plover/plover"
license=('GPLv2')
groups=()
depends=('python2' 'wxpython' 'python2-xlib' 'wmctrl'
    'python2-simplejson' 'python2-pyserial' 'python2-appdirs')
makedepends=('git')
provides=('plover')
conflicts=()
replaces=()
backup=()
options=()
install=
source=('git+https://github.com/plover/plover.git')
noextract=()
md5sums=('SKIP')

pkgver() {
    cd $_gitname
    git describe --tags --always | sed 's/-/./g'
}

build() {
    cd $_gitname
    python2 setup.py build
}

package() {
    cd $_gitname
    python2 setup.py install --root="$pkgdir"
}
