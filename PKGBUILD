# Maintainer: Aleksej Komarov <stylemistake@gmail.com>
# Maintainer: MKzero <info[at]linux-web-development[dot]de>
# Upstream: Bitwig GmbH <support@bitwig.com>

# If you find problems with the package, create an issue on Github:
# https://github.com/stylemistake/bitwig-studio-aur

pkgname='bitwig-studio'
pkgver='2.2.3'
_pkgver='2.2.3'
pkgrel='1'
pkgdesc='Digital audio workstation for music production, remixing and live performance'
arch=('x86_64')
url='https://www.bitwig.com/'
license=('custom')
depends=('jack' 'xdg-utils' 'zenity' 'xcb-util-wm' 'libbsd')
optdepends=('alsa-lib' 'oss' 'ffmpeg: MP3 support')
provides=('bitwig-studio')
replaces=()
conflicts=('bitwig-studio-legacy' 'bitwig-8-track')
options=(!strip)
source=("https://downloads.bitwig.com/stable/${_pkgver}/bitwig-studio-${_pkgver}.deb")
md5sums=('fe5b43ba07c0d24c462b50b97b133d0c')

package() {
  # Unpack package contents
  bsdtar -xf ${srcdir}/data.tar.xz -C ${pkgdir}/

  # Install license
  install -D -m644 ${pkgdir}/opt/bitwig-studio/EULA.rtf ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
