# Maintainer : Ionut Biru <ibiru@archlinux.org>
# Contributor: Alex Anthony <alex.anthony28991@gmail.com>

pkgname=python-markupsafe
pkgver=0.9.2
pkgrel=1
pkgdesc="Implements a XML/HTML/XHTML Markup safe string for Python"
arch=('i686' 'x86_64')
url="http://pypi.python.org/pypi/MarkupSafe"
license=('custom')
depends=('python')
makedepends=('setuptools')
source=(http://pypi.python.org/packages/source/M/MarkupSafe/MarkupSafe-${pkgver}.tar.gz)
md5sums=('69b72d1afdd9e808f9c1ef65f819c7a6')

build() {
  cd ${srcdir}/MarkupSafe-${pkgver}
  python setup.py install --root=${pkgdir} --optimize=1

  install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
