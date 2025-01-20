pkgname=gui-scale-applet
pkgver=2.0.0
pkgrel=1
pkgdesc="A secure, memory-safe implementation of a Tailscale GUI management applet for the System76 COSMIC desktop environment."
arch=('x86_64')
url="https://github.com/pop-os/gui-scale-applet"
license=('BSD')
depends=('rust' 'cargo' 'libxkbcommon')
source=("$pkgname-$pkgver.tar.gz::https://github.com/pop-os/gui-scale-applet/archive/v$pkgver.tar.gz")
sha256sums=('replace_with_real_checksum')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 "target/release/gui-scale-applet" "$pkgdir/usr/bin/gui-scale-applet"
}
