# Maintainer: Catalin Boldan <catalin.boldan@gmail.com>
pkgname=system-sleep-with-vms
pkgver=1.1
pkgrel=1
pkgdesc="Qemu guest suspend and resume if the host systems gets suspended/resumed."
arch=('any')
url="https://github.com/BFCatalin/system-sleep-with-vms"
license=('GPL2')
depends=(libvirt)
makedepends=('git')
source=("$pkgname::git+https://github.com/BFCatalin/system-sleep-with-vms")
noextract=()
sha256sums=('SKIP')

build() {
  cd "$pkgname"
}

package() {
  cd "$pkgname"
  install -Dm755 ./system-sleep-resume-suspended "$pkgdir/usr/bin/system-sleep-resume-suspended"
  install -Dm755 ./system-sleep-suspend-running "$pkgdir/usr/bin/system-sleep-suspend-running"
	install -Dm644 ./root-resume.service "$pkgdir/usr/lib/systemd/system/root-resume.service"
  install -Dm644 ./root-suspend.service "$pkgdir/usr/lib/systemd/system/root-suspend.service"
}
