# Maintainer: Jeff Youdontneedtoknow <jeffpublicjr at gmail dot com>
pkgname=heli-x5
pkgver=5.0.1401
pkgrel=4
pkgdesc="Older depreciated professional R/C helicopter flight simulator from Heli-x"
arch=("i686" "x86_64")
url="http://www.heli-x.net/"
license=('custom')
depends=('java-environment-common' 'lib32-libxcursor' 'lib32-libxrandr' 'bash' 'lib32-libxxf86vm')
makedepends=('imagemagick')
source=('heli-x5' 'heli-x5.desktop' 'http://www.heli-x.info/1405/HELI-X5.tar.gz')
md5sums=('ca1d8dd7672d28352e59efab5ade0abc'
         'fd7165cc8b1eb16956d616722c46152f'
         '954c7c4123800c1bc9247294f5b2b791')
options=(!strip)

package() {
  install -d -m755 $pkgdir/usr/share/
  cp -R HELI-X5 $pkgdir/usr/share/$pkgname
  install -d -m755 $pkgdir/usr/bin
  install -m755 heli-x5 $pkgdir/usr/bin/$pkgname
  install -d -m755 $pkgdir/usr/share/applications
  install -d -m755 $pkgdir/usr/share/pixmaps
  install -m755 $pkgname.desktop $pkgdir/usr/share/applications
  convert $srcdir/HELI-X5/runHELI-X.ico runHELI-X-3.png
  install -m755 $srcdir/runHELI-X-3-3.png $pkgdir/usr/share/pixmaps/$pkgname.png
  install -d -m755 $pkgdir/usr/share/licenses/$pkgname
  install -m755 $srcdir/HELI-X5/libs/HeliX/license.txt $pkgdir/usr/share/licenses/$pkgname/license.text
  install -m755 $srcdir/HELI-X5/libs/HeliX/license_e.txt $pkgdir/usr/share/licenses/$pkgname/license_e.text
  }

 
