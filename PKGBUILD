# Maintainer: Limao Luo <luolimao+AUR@gmail.com>
# Contributor: sausageandeggs <sausageandeggs@archlinux.us>
# Contributor: Christoph Zeiler <archNOSPAM@moonblade.org>
# Contributor: Nathan Owe <ndowens04+AUR@gmail.com>

pkgname=cbrpager
pkgver=0.9.22
pkgrel=2
pkgdesc="A no-nonsense, simple to use, small viewer for cbr and cbz files, written in C"
arch=(i686 x86_64)
url=http://sourceforge.net/projects/$pkgname/
license=(GPL2)
depends=(libgnomeui)
source=(http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz)
sha256sums=('1852303374d7777f2a5f395fda97d78f970fa87c854ee048495a901922b7dd84')
sha512sums=('dc4bcf14528e6708a3ff0fc3b7e3163dfb9d6063f1cf40545b4f804915afedd9db4cd461834de7ee92fcd4b2f302b7f2ed0d9ae022e220dd8e6c95ccabea34d5')

build() {
    cd $pkgname-$pkgver/
    ./configure --prefix=/usr
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}
