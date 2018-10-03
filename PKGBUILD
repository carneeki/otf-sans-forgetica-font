# Maintainer: Adam Carmichael <carneeki at carneeki dot net>

_pkgname=SansForgeticaFont

pkgname=otf-sans-forgetica-font
pkgver=1.0
pkgrel=1
pkgdesc="A font that is scientifically designed to help you remember your study notes."
arch=('any')
url="https://github.com/carneeki/SansFranciscoFont"
license=('unknown')
groups=()
depends=()
makedepends=()
provides=($_pkgname)
source=('https://www.sansforgetica.com.au/Common/Zips/Sans%20Forgetica.zip')
md5sums=('SKIP')

pkgver() {
    cd "$srcdir/Sans\ Forgetica/"
    git describe --tags --long | sed -r -e 's,^[^0-9]*,,;s,([^-]*-g),r\1,;s,[-_],.,g'
}

package() {
    cd "$srcdir/$_pkgname"
    install -d "$pkgdir/usr/share/fonts/OTF"
    install -m644 *.otf "$pkgdir/usr/share/fonts/OTF"
}
