pkgname=guvcview
pkgver=2.0.4
pkgrel=1
pkgdesc="A video viewer and capturer for the linux uvc driver"
arch=('x86_64')
url="http://guvcview.sourceforge.net/"
license=('GPL')
depends=('portaudio' 'ffmpeg' 'gtk3' 'sdl2' 'gsl')
makedepends=('pkg-config' 'intltool')
optdepends=('pulseaudio: for PulseAudio support')
options=('!docs' '!buildflags')
source=("http://downloads.sourceforge.net/project/${pkgname}/source/${pkgname}-src-${pkgver}.tar.gz")
md5sums=('a6d900166ac2bba251a2c09cb602f1fe')

build() {
  cd ${pkgname}-src-${pkgver}

  ./configure --prefix=/usr \
              --disable-debian-menu
  make
}

package() {
  cd ${pkgname}-src-${pkgver}

  make DESTDIR="${pkgdir}" install
}
