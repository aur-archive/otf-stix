# Maintainer: ezzetabi <ezzetabi at gawab dot com>

pkgname=otf-stix
pkgver=1.1.1_webfonts
_pkgver=${pkgver//_/-}
pkgrel=1
epoch=3
pkgdesc='A comprehensive set of fonts that serve the scientific and engineering community.'
arch=('any')
url="http://www.stixfonts.org"
license=('custom:STIXFont')
depends=('fontconfig' 'xorg-fonts-encodings' 'xorg-font-utils')
makedepends=('unzip')
install=otf-stix.install
source=("http://downloads.sourceforge.net/stixfonts/STIXv$_pkgver.zip"
'http://www.stixfonts.org/STIXFontLicense2010.txt')

package() {
  cd "$srcdir"

  install -m755 -d "$pkgdir/usr/share/fonts/OTF"
  install -m644 ./STIX-MathJax/otf/*.otf "$pkgdir/usr/share/fonts/OTF"
  install -Dm644 "$srcdir"/STIXFontLicense2010.txt \
    "$pkgdir"/usr/share/licenses/"$pkgname"/license.txt
}

md5sums=('5673808f48b1e5ab77064a3585866aab'
'b1af7bbd3cea93a60bf68cf571ad6cab')
