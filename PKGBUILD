pkgname=guvcview
pkgver=1.7.3
pkgrel=1
pkgdesc="A video viewer and capturer for the linux uvc driver"
arch=('x86_64')
url="http://guvcview.sourceforge.net/"
license=('GPL')
depends=('portaudio-svn' 'ffmpeg' 'gtk3')
makedepends=('pkg-config' 'intltool')
optdepends=('pulseaudio: for PulseAudio support')
options=('!docs')
source=("http://downloads.sourceforge.net/project/${pkgname}/source/${pkgname}-src-${pkgver}.tar.gz")
md5sums=('f9c510ed9908a8d20ca27099aca948a7')

build() {
  cd "${srcdir}/${pkgname}-src-${pkgver}"

  ./configure --prefix=/usr \
              --disable-debian-menu
  make
}

package() {
  cd "${srcdir}/${pkgname}-src-${pkgver}"

  make DESTDIR="${pkgdir}" install
}