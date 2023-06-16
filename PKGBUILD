# Maintainer: gobonja <gobonja@gmail.com>

pkgname=timeshift-autosnap
pkgver=1.0
pkgrel=1
pkgdesc="Timeshift auto-snapshot script which runs before package upgrade using Pacman hook."
arch=("any")
url="https://github.com/bkmo/${pkgname}"
license=('MIT')
depends=('timeshift')
optdepends=('grub-btrfs')
source=("${pkgname}-${pkgver}.tar.gz::${url}/archive/${pkgver}.tar.gz")
b2sums=('SKIP')
backup=('etc/timeshift-autosnap.conf')

package() {
    cd ${srcdir}/${pkgname}-${pkgver}
    install -Dm644 00-timeshift-autosnap.hook ${pkgdir}/usr/share/libalpm/hooks/00-timeshift-autosnap.hook
    install -Dm644 timeshift-autosnap.conf ${pkgdir}/etc/timeshift-autosnap.conf
    install -Dm755 timeshift-autosnap ${pkgdir}/usr/bin/timeshift-autosnap
    install -Dm644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
 
