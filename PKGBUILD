# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=anki-last-stable
pkgver=2.1.22
pkgrel=1
epoch=
pkgdesc="Version 2.1.22 of Anki"
arch=('x86_64')
url="https://apps.ankiweb.net"
license=('AGPL3')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=('mpv: play audio'
            'lame: record audio')
provides=('anki=2.1.22')
conflicts=('anki' 'anki20')
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/ankitects/anki/releases/download/$pkgver/anki-$pkgver-linux-amd64.tar.bz2")
noextract=()
md5sums=('d056f300d36d5ce6722653d260deb0fa')
validpgpkeys=()

prepare() {
	cd "anki-$pkgver-linux-amd64"
}

build() {
	cd "anki-$pkgver-linux-amd64"
	make
}

package() {
	cd "anki-$pkgver-linux-amd64"
	sudo make PREFIX="$pkgdir/usr/local" install
}
