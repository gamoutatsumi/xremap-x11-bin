# Maintainer: Tatsumi Gamou <tatsumigamou@protonmail.com>
pkgname=xremap-x11-bin
pkgver=0.1.2
pkgrel=1
pkgdesc="Dynamic key remapper for X11 and Wayland"
arch=("x86_64")
url="https://github.com/k0kubun/xremap"
license=('MIT')
depends=("libx11")
source=("https://github.com/k0kubun/${pkgname/-x11-bin}/releases/download/v${pkgver}/${pkgname/-x11-bin}-linux-x86_64-x11.zip" "xremap.service")
sha256sums=('86f28c411dc23619aa9d17dd42d6f21823f7ba04faf86cc1b830938580d2d777'
            '7e6c236b36619a2e8bf63c8423e453cd0d3f07721f00c5d8d244569dca1249f4')

package() {
  install -Dm755 "${srcdir}/${pkgname/-x11-bin}" "${pkgdir}/usr/bin/${pkgname/-x11-bin}"
  install -Dm644 xremap.service -t "${pkgdir}/usr/lib/systemd/user"
}
