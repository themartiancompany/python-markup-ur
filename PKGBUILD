# Maintainer : Ionut Biru <ibiru@archlinux.org>
# Contributor: Alex Anthony <alex.anthony28991@gmail.com>

pkgname=('python-markupsafe' 'python2-markupsafe')
pkgver=0.15
pkgrel=1
pkgdesc="Implements a XML/HTML/XHTML Markup safe string for Python"
arch=('i686' 'x86_64')
url="http://pypi.python.org/pypi/MarkupSafe"
license=('custom')
makedepends=('python-distribute' 'python2-distribute')
source=("http://pypi.python.org/packages/source/M/MarkupSafe/MarkupSafe-${pkgver}.tar.gz")
md5sums=('4e7c4d965fe5e033fa2d7bb7746bb186')

build() {
  cp -r MarkupSafe-${pkgver} python2-MarkupSafe-${pkgver}
  cd ${srcdir}/MarkupSafe-${pkgver}
  python setup.py build

  cd ${srcdir}/python2-MarkupSafe-${pkgver}
  python2 setup.py build
}

package_python-markupsafe() {
  depends=('python')

  cd ${srcdir}/MarkupSafe-${pkgver}
  python setup.py install --root=${pkgdir} --optimize=1

  install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/python-markupsafe/LICENSE
}

package_python2-markupsafe() {
  depends=('python2')

  cd ${srcdir}/python2-MarkupSafe-${pkgver}
  python2 setup.py install --root=${pkgdir} --optimize=1

  install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/python2-markupsafe/LICENSE
}
