# Suckless Terminal Scroll

pkgname=scroll
pkgver=git
pkgrel=1
pkgdesc='Suckless Terminal Scroll'
arch=('x86_64')
license=('ISC')
depends=()
url=https://git.suckless.org/scroll

_makeopts="--directory=$BUILDDIR"

build() {
  make $_makeopts
}

package() {
  local installopts="--mode 0644 -D --target-directory"
  local shrdir="$pkgdir/usr/share"
  local licdir="$shrdir/licenses/$pkgname"
  local docdir="$shrdir/doc/$pkgname"
  make $_makeopts PREFIX=/usr DESTDIR="$pkgdir" install
  install $installopts "$licdir" "$BUILDDIR/LICENSE"
  install $installopts "$docdir" "$BUILDDIR/README"
}
