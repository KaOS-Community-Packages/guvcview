pkgname=guvcview
pkgver=2.0.1
pkgrel=1
pkgdesc="A video viewer and capturer for the linux uvc driver"
arch=('x86_64')
url="http://guvcview.sourceforge.net/"
license=('GPL')
depends=('portaudio-svn' 'ffmpeg' 'gtk3' 'sdl2' 'gsl')
makedepends=('pkg-config' 'intltool')
optdepends=('pulseaudio: for PulseAudio support')
options=('!docs' '!buildflags')
source=("http://downloads.sourceforge.net/project/${pkgname}/source/${pkgname}-src-${pkgver}.tar.gz")
md5sums=('54e608b8a2c13d96f546197117d758f4')

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