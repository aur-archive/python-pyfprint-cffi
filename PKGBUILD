# Maintainer: Francisco Demartino <demartino.francisco@gmail.com>

# based on python-pyfprint-git PKGBUILD
# Contributors: Bruno Gomes <bgomes@opens1.com>, Lucas Castro <lucas@opens1.com>

pkgname=python-pyfprint-cffi
pkgver=r32.3caef8c
pkgrel=1
pkgdesc="CFFI bindings libfprint fingerprinting library"
url="https://github.com/franciscod/pyfprint"
arch=('i686' 'x86_64')
license=('GPL-2')
depends=('python' 'libfprint')
makedepends=('python-cffi')
source=("git+https://github.com/franciscod/pyfprint.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/pyfprint"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "${srcdir}/pyfprint"
  python setup.py build
}

package() {
  cd "${srcdir}/pyfprint"
  python setup.py install --root=${pkgdir}
}
