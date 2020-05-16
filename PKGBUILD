# Maintainer: John Lindgren <john@jlindgren.net>

pkgname=volumeicon-gtk2
pkgver=0.5.1+git
pkgrel=1
pkgdesc='Volume control for your system tray (GTK2 version)'
arch=('x86_64')
url='https://github.com/jlindgren90/volumeicon-gtk2'
license=('GPL3')
depends=('gtk2' 'alsa-lib' 'libnotify')
makedepends=('intltool')
provides=('volumeicon')
conflicts=('volumeicon')
replaces=('volumeicon')

build() {
  cd ..
  ./autogen.sh
  ./configure --prefix=/usr --enable-notify
  make
}

package() {
  cd ..
  make DESTDIR="$pkgdir" install
}
