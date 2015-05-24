# Maintainer: Patrick Wozniak <hello@patwoz.de>

pkgname=pi-blaster-git
pkgver=20140715.111.485c939
pkgrel=1
pkgdesc="Daemon for Raspberry Pi which provides an interface to drive multiple PWM via the GPIO pins"
arch=('any')
url="https://github.com/sarfata/pi-blaster/"
license=('MIT')
makedepends=('git')
source=("git+https://github.com/sarfata/${pkgname%-*}")
sha1sums=('SKIP')

pkgver() {
  cd "${pkgname%-*}"
  echo "$(date +%Y%m%d).$(git rev-list --count master).$(git rev-parse --short master)"
}

prepare() {
    cd "${pkgname%-*}"
    ./autogen.sh
}

build() {
    cd "${pkgname%-*}"
    ./configure
    make
}

package() {
    cd "${pkgname%-*}"
    make DESTDIR="${pkgdir}" install
}
