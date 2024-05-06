# Maintainer: Piotr Miller <nwg.piotr@gmail.com>
pkgname=('autotiling')
pkgver=1.9.2
pkgrel=2
pkgdesc="Script for sway and i3 to automatically switch the horizontal / vertical window split orientation"
arch=('any')
url="https://github.com/nwg-piotr/autotiling"
license=('GPL3')
provides=('autotiling')
depends=('python-i3ipc')
makedepends=('python-setuptools' 'python-wheel')
source=("$pkgname-$pkgver.tar.gz::https://github.com/nwg-piotr/autotiling/archive/v$pkgver.tar.gz")

md5sums=('a26998419cdbd8bf3beb363801996843')

package() {
  cd "${pkgname}-${pkgver}"
  python setup.py install --root="${pkgdir}" --optimize=1
  
  install -D -t "$pkgdir"/usr/share/licenses/"$pkgname" LICENSE
  install -D -t "$pkgdir"/usr/share/doc/"$pkgname" README.md
}
