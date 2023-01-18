# Maintainer: elementh <hello@lucasmarino.me>
pkgname=anytype-bin
pkgver=0.30.0
pkgrel=1
pkgdesc="Operating environment for the new internet. Anytype is a next generation software that breaks down barriers between applications, gives back privacy and data ownership to users."
arch=('x86_64')
url="https://anytype.io/"
license=('custom')
depends=('fuse')
options=(!strip)
optdepends=('org.freedesktop.secrets: for not having to sign in each time')
provides=('anytype')
conflicts=('anytype')
_appimage="Anytype-${pkgver}.AppImage"
source=(
    "Anytype-${pkgver}.AppImage::https://at9412003.fra1.digitaloceanspaces.com/Anytype-${pkgver}.AppImage"
    "anytype.desktop"
    "anytype.png"
    )
noextract=("${_appimage}")
sha256sums=('2e27c973998b6e7b79c015c63359f5ba271ed01ea6098f342d87f7904149cbdd'
            '1bda1398291bed84ebee1d2c3e94b4c367925a8e2c0bd371aba8d6604e54281f'
            '48ee23a45c29cf081ccf5188c045150b7410007cd21743ce8592974ab18120c0')

package() {
    install -Dm755 $_appimage "$pkgdir"/usr/bin/anytype
    chmod +x "${pkgdir}/usr/bin/anytype"

    install -Dm644 "anytype.desktop"                    "${pkgdir}/usr/share/applications/anytype.desktop"
    install -Dm644 "anytype.png"                        "${pkgdir}/usr/share/icons/hicolor/128x128/apps/anytype.png"
}
