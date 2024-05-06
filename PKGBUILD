pkgname=refilc
pkgver=4.5.2
pkgrel=1
pkgdesc="Nem hivatalos e-napló alkalmazás az e-KRÉTA rendszerhez - tanulóktól, tanulóknak."
arch=('x86_64')
url="https://github.com/refilc/naplo"
options=(!debug strip)
license=('AGPL-3.0')
provides=('refilc')
conflicts=('refilc')
source=("https://github.com/pml68/naplo/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('SKIP')

package() {
  mkdir -p $pkgdir/opt/refilc
  install -Dm755 "$srcdir/filcnaplo" "$pkgdir/opt/refilc/refilc"
  cp -rf "$srcdir/lib" "$pkgdir/opt/refilc"
  cp -rf "$srcdir/data" "$pkgdir/opt/refilc"
  [[ -h "/usr/bin/refilc" ]] || ln -s /opt/refilc/refilc /usr/bin/refilc
}
