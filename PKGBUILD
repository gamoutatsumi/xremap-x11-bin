# Maintainer: Tatsumi Gamou <tatsumigamou at protonmail dot com>
pkgname=xremap-x11-bin
pkgver=0.2.5
pkgrel=3
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=('66e3cf1c40d3953286aacfacb2d1a73d30fd3d50d29a565f959eb9c7d4cc3917'
            'c39aa3f7bc9fc8e91f514eb6bd959ee549e3c9525e0a369648651d119cf55b85')

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/system"
}
