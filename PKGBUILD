# Maintainer: Tatsumi Gamou <tatsumigamou at protonmail dot com>
pkgname=xremap-x11-bin
pkgver=0.3.1
pkgrel=1
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=('2fc3ee39d21d5f68a4d9459d0d71ddf34c317fdf21f20cddb254ca4a382aabe5'
            'c39aa3f7bc9fc8e91f514eb6bd959ee549e3c9525e0a369648651d119cf55b85')

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/system"
}
