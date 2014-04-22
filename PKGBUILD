# Maintainer : Felix Yan <felixonmars@gmail.com>
# Contributor: Ionut Biru <ibiru@archlinux.org>
# Contributor: Alex Anthony <alex.anthony28991@gmail.com>

pkgname=('python-markupsafe' 'python2-markupsafe')
pkgver=0.21
pkgrel=1
pkgdesc="Implements a XML/HTML/XHTML Markup safe string for Python"
arch=('i686' 'x86_64')
url="http://pypi.python.org/pypi/MarkupSafe"
license=('custom')
makedepends=('python-setuptools' 'python2-setuptools')
source=("http://pypi.python.org/packages/source/M/MarkupSafe/MarkupSafe-${pkgver}.tar.gz")
sha512sums=('ecedf56be7ad1723c4d7bf799e1aefb8ceb0a28840a1b8ffdc2dee0f734149430cf5dfd5d335591e9934cf223255475e9c04da5ab34ed69e7845298f599d81bc')

build() {
  cp -r MarkupSafe-${pkgver} python2-MarkupSafe-${pkgver}
  cd "${srcdir}/MarkupSafe-${pkgver}"
  python setup.py build

  cd "${srcdir}/python2-MarkupSafe-${pkgver}"
  python2 setup.py build
}

check() {
  cd "${srcdir}/MarkupSafe-${pkgver}"
  python setup.py test

  cd "${srcdir}/python2-MarkupSafe-${pkgver}"
  python2 setup.py test
}

package_python-markupsafe() {
  depends=('python')

  cd MarkupSafe-${pkgver}
  python setup.py install --root="${pkgdir}" --optimize=1

  install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/python-markupsafe/LICENSE"
}

package_python2-markupsafe() {
  depends=('python2')

  cd python2-MarkupSafe-${pkgver}
  python2 setup.py install --root="${pkgdir}" --optimize=1

  install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/python2-markupsafe/LICENSE"
}
