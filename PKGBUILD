# Maintainer: Voobscout <voobscout+aur@gmail.com>
pkgname=xorg-xfs-showfont
pkgver=1.0.5
pkgrel=1
pkgdesc="X Font Server - show font"
arch=('i686' 'x86_64')
license=('GPL2')
makedepends=('git' 'pkg-config' 'autoconf' 'automake' 'gettext' 'xproto' 'xtrans' 'wget')
#depends=('libfs')
url="http://xorg.freedesktop.org/archive/individual/app"
provides=('xorg-xfs-showfont')
optdepends=('xorg-xfs' 'xorg-xfstt')
source=("http://xorg.freedesktop.org/archive/individual/app/showfont-$pkgver.tar.gz")
sha256sums=('566e34a145ea73397724d46e84f6a9b3691cf55d0fcb96ec7f917b2b39265ebb')
options=(!strip)

build() {
  cd ${srcdir}/showfont-${pkgver}
  msg "Configuring fslsfonts..."
  ./configure --prefix=/usr
  msg "Compiling XFS... "
  make
}

package() {
  msg "Installing fslsfonts"
  cd ${srcdir}/showfont-${pkgver}
  make DESTDIR=${pkgdir} install
}

# vim:set ts=2 sw=2 et:
