# Maintainer: Limao Luo <luolimao@gmail.com>
# Contributor: William Rea <sillywilly@gmail.com>
# Contributor: Roman Kyrylych <roman@archlinux.org>
# Contributor: Lucas Saliés Brum <lucas@archlinux.com.br>

pkgname=nautilus-locked-folder
pkgver=8
pkgrel=2
pkgdesc="A plugin that allows to encrypt the contents of a folder using the Blowfish algorithm"
arch=(i686 x86_64)
url="https://www.gnome.org/projects/nautilus-locked-folders"
license=(GPL2)
depends=(nautilus libglade libgnomeui eel-language)
makedepends=(subversion gnome-common intltool)
options=(!libtool !emptydirs)
source=($pkgname.tar.bz2::'https://dl.dropbox.com/sh/vjz5en03wxqzxbq/F3R-u28zQE/$pkgname.tar.bz2?dl=1')
sha256sums=('e009c3b736d5872ba0b7fb5636ebd75c8099312e919abd2c8dac12e9d2a3df56')
sha512sums=('3e39cdb929d1abea8e611a89fdcab499e628e25f1fded8a3a9101eb7f7e5151c4df0ae6b0a655318d61e435c49a1b347a7c29d53fe731d161effaf07400c291d')

build() {
    cd $srcdir/$pkgname/
    autogen.sh --prefix=/usr --sysconfdir=/etc --localstatedir=/var
    make
}

package() {
    cd $pkgdir/$pkgname/
    make DESTDIR=$pkgdir install
}
