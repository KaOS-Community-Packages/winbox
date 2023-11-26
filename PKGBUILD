pkgname=winbox
pkgver=3.40
pkgrel=1
pkgdesc="Winbox is an utility that allows the administration of MikroTik RouterOS usings GUI. (Wine)"
url="https://mikrotik.com"
arch=('x86_64')
license=('custom')
depends=('wine')
optdepends=('ttf-ms-fonts: for better fonts')
install=${pkgname}.install
source=("${pkgname}-${pkgver}.exe::https://download.mikrotik.com/winbox/${pkgver}/${pkgname}64.exe"
        "${pkgname}.desktop"
        "${pkgname}.png"
        "${pkgname}")
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
  install -Dm755 "${srcdir}/${pkgname}-${pkgver}.exe" "${pkgdir}/usr/share/${pkgname}/${pkgname}.exe"
  install -Dm755 "${srcdir}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
  install -Dm655 "${srcdir}/${pkgname}.png" "${pkgdir}/usr/share/pixmaps/${pkgname}.png"
  install -Dm655 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications/${pkgname}.desktop"
}
