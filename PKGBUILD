# Maintainer: Tatsumi Gamou <tatsumigamou at protonmail dot com>
pkgname=xremap-x11-bin
pkgver=0.2.2
pkgrel=1
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=('a8975a7fcb30de25dea89ea9be0a77153447ff39dd1d9a4b1dcee96c8efc58b8'
            'bcbdde63f4925534d1613b8399142f728bc2599a3bb969a22dca78d6ee83e13f')

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/user"
}
