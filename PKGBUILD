# Maintainer: Tatsumi Gamou <tatsumigamou@protonmail.com>
pkgname=xremap-x11-bin
pkgver=0.1.0
pkgrel=1
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=("4937387a1e3b9531d97750c5971d3a45a46e62065a4dc10ee4503c7dffbf2dd1" "7e6c236b36619a2e8bf63c8423e453cd0d3f07721f00c5d8d244569dca1249f4")

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/user"
}
