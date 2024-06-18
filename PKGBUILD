# Maintainer: Piotr Miller <nwg.piotr@gmail.com>
pkgname=('autotiling')
pkgver=1.9.3
pkgrel=1
pkgdesc="Script for sway and i3 to automatically switch the horizontal / vertical window split orientation"
arch=('any')
url="https://github.com/nwg-piotr/autotiling"
license=('GPL3')
provides=('autotiling')
depends=('python-i3ipc')
makedepends=('python-build' 'python-installer' 'python-wheel' 'python-setuptools')
source=("$pkgname-$pkgver.tar.gz::https://github.com/nwg-piotr/autotiling/archive/v$pkgver.tar.gz")

md5sums=('03e10a3ea96e6899b1da84a1c61d480b')

build() {
        cd "${pkgname}-${pkgver}"
        python -m build --wheel --no-isolation
}

package() {
  cd "${pkgname}-${pkgver}"
  python -m installer --destdir="${pkgdir}" dist/*.whl
  
  install -D -t "$pkgdir"/usr/share/licenses/"$pkgname" LICENSE
  install -D -t "$pkgdir"/usr/share/doc/"$pkgname" README.md
}
