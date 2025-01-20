pkgname=gui-scale-applet
pkgver=2.0.0
pkgrel=1
pkgdesc="A secure, memory-safe implementation of a Tailscale GUI management applet for the System76 COSMIC desktop environment."
arch=('x86_64')
url="https://github.com/cosmic-utils/gui-scale-applet"
license=('BSD')
depends=('rust' 'cargo' 'libxkbcommon')
source=("$pkgname-$pkgver.tar.gz::https://github.com/cosmic-utils/gui-scale-applet/archive/refs/tags/2.0.0.tar.gz")
sha256sums=('db210c32f84cf191923c736236bf99500dc24e8ee990ffdf9c382f8d4074945c')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 "target/release/gui-scale-applet" "$pkgdir/usr/bin/gui-scale-applet"
}
