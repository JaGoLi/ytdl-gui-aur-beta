# Maintainer: Jason Goulet-Lipman <jason.gouletlipman@gmail.com>

pkgname=youtubedl-gui-git
pkgver=2.0.r0.g0bbc2c1
pkgrel=1
arch=(x86_64)
url="https://github.com/JaGoLi/ytdl-gui"
license=(GPL3)
depends=(youtube-dl qt5-base ffmpeg)
makedepends=(git qt5-quickcontrols)
provides=(youtubedl-gui)
conflicts=(youtubedl-gui)
source=("git+https://github.com/JaGoLi/ytdl-gui#branch=beta")
sha256sums=('SKIP')

pkgver(){
  	cd ytdl-gui
    git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

build() {
	cd ytdl-gui
	make build
}

package() {
	cd ytdl-gui
	make DESTDIR="${pkgdir}/" install
}
