# Maintainer: Alan Jenkins <alan.james.jenkins@gmail.com>

pkgname=atlauncher
pkgver=latest
pkgrel=1
pkgdesc="The ATLauncher Minecraft mod pack manager and launcher."
arch=('i686' 'x86_64')
url="http://www.atlauncher.com"
license=('CCPL')
depends=('java-runtime' 'xorg-server-utils' 'openal')
provides=('atlauncher')

install='atlauncher.install'

source=("http://www.atlauncher.com/downloadfile.php?file=jar"
        "")

md5sums=()

package() {
    cd "$srcdir"

    install -D -m755 "${srcdir}/atlauncher"         "${pkgdir}/usr/bin/atlauncher"
    install -D -m644 "${srcdir}/ATLauncher.jar"     "${pkgdir}/usr/share/atlauncher/ATLauncher.jar"

    # Desktop launcher with icon
    install -D -m644 "${srcdir}/atlauncher.desktop" "${pkgdir}/usr/share/applications/atlauncher.desktop"
    install -D -m644 "${srcdir}/atlauncher.png"     "${pkgdir}/usr/share/pixmaps/atlauncher.png"

    # License
    install -D -m644 "${srcdir}/LICENSE"           "${pkgdir}/usr/share/licenses/atlauncher/LICENSE"
}

# vim:set ts=4 sw=4 et:
