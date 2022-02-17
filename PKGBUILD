# Maintainer: Catalin Boldan <me@kstep.me>
pkgname=system-sleep-with-vms
pkgver=1.0
pkgrel=1
pkgdesc=""
arch=('x86_64')
url="https://github.com/BFCatalin/system-sleep-with-vms"
license=('GPL2')
#groups=()
depends=(libvirt)
makedepends=('git')
#optdepends=()
#provides=()
#conflicts=()
#replaces=()
#backup=()
#options=()
#install=
#changelog=
source=($pkgname::git+https://github.com/BFCatalin/system-sleep-with-vms)
noextract=()
md5sums=() #generate with 'makepkg -g'

pkgver() {
	cd "$srcdir/system-sleep-with-vms"
	git log -1 --format="%cd" --date=short | sed 's|-||g'
}

build() {
  cd "$pkgname"
}

package() {
  cd "$pkgname"
	install -Dm755 ./root-resume.service "$pkgdir/lib/systemd/system"
  install -Dm755 ./root-suspend.service "$pkgdir/lib/systemd/system"
}
