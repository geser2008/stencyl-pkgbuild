# Maintainer: SanskritFritz (gmail)
# Contributor: Sander Smid-Merlijn <sander..smid@gmail.com>
# Maintainer: geser2008  distselemov at gmail dot com
pkgname=stencyl
pkgver=4.1.4
pkgrel=1
pkgdesc='Create amazing games without code.'
arch=('x86_64')
url='http://www.stencyl.com'
license=(custom)
options=('!strip')
source=("https://static.stencyl.com/downloads/stencyl/release/$pkgver/Stencyl-$pkgver.zip"
        "stencyl"
        "stencyl.desktop"
        "stencyl.png")
md5sums=('f4140a72f30d7529bcc32829290306d1'
         '140d00efc46d7a35068ac24c5b9bbf43'
         '6b52a9ecce3bddda2e77b3884503b888'
         'c99ae55db267e86c0936e01662ee12ea')

package() {
    install -Ddm755 "$pkgdir"/usr/share
    cp -r "Stencyl-$pkgver" "$pkgdir"/usr/share/stencyl

    # Install the custom launch script, the .desktop and the icon
    install -Dm755 "$srcdir/stencyl" "$pkgdir/usr/bin/stencyl"
    install -Dm755 "$srcdir/stencyl.desktop" "$pkgdir/usr/share/applications/stencyl.desktop"
    install -Dm644 "$srcdir/stencyl.png" "$pkgdir/usr/share/pixmaps/stencyl.png"

}
