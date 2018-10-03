# Maintainer: Adam Carmichael <carneeki at carneeki dot net>

_pkgname=SansForgeticaFont

pkgname=otf-sans-forgetica-font
pkgver=r6.f418d8c
pkgrel=1
pkgdesc="A font that is scientifically designed to help you remember your study notes."
arch=('any')
url="https://github.com/carneeki/otf-sans-forgetica-font"
license=('unknown')
groups=()
depends=()
makedepends=()
provides=($_pkgname)
source=('https://www.sansforgetica.com.au/Common/Zips/Sans%20Forgetica.zip')
md5sums=('SKIP')

prepare() {
    cd "$srcdir"
    mv "Sans Forgetica" $_pkgname
}

pkgver() {
    cd "$_pkgname"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "$srcdir/$_pkgname"
    install -d "$pkgdir/usr/share/fonts/OTF"
    install -m644 *.otf "$pkgdir/usr/share/fonts/OTF"
}
