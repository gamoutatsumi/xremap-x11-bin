# Maintainer: Tatsumi Gamou <tatsumigamou at protonmail dot com>
pkgname=xremap-x11-bin
pkgver=0.2.2
pkgrel=2
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=('a8975a7fcb30de25dea89ea9be0a77153447ff39dd1d9a4b1dcee96c8efc58b8'
            '6564e7d4f9b37af9ea7b5e724b746f08da9a419059c19c62b305e78cd3caab4a')

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/user"
}
