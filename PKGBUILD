# Maintainer: Tatsumi Gamou <tatsumigamou@protonmail.com>
pkgname=xremap-x11-bin
pkgver=0.1.1
pkgrel=1
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=("c7234b99255fcc201d658636ee3c5eddaef79e7f41daa2d606869bf490acb9f6" "7e6c236b36619a2e8bf63c8423e453cd0d3f07721f00c5d8d244569dca1249f4")

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/user"
}
