pkgname=reboot-mode
pkgver=1.0.0
pkgrel=1
pkgdesc="Reboot the device to a specific mode"
url="https://gitlab.com/postmarketOS/reboot-mode"
arch=(any)
license=(GPL3)
makedepends=(linux-headers)
source=("https://gitlab.com/postmarketos/reboot-mode/-/archive/$pkgver/reboot-mode-$pkgver.tar.gz")


build() {
  cd "${srcdir}/reboot-mode-$pkgver"
	${CC:-gcc} $CFLAGS reboot-mode.c -o reboot-mode.o -c
	${CC:-gcc} $CFLAGS reboot-mode.o -o reboot-mode
}

package() {
	install -Dm755 "${srcdir}/reboot-mode-$pkgver"/reboot-mode \
		"$pkgdir"/usr/bin/reboot-mode
}

sha512sums=("926fae6f1b78b144f092d291f1d0edf58f2a5ea98d3af7aa812f4f1e1330002feb5a8c4499fe334e6d22bc515467359a5a0651e3995d2217a844f3c1b668ae9b")
