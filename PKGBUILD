# Maintainer: Alex Brinister <alex_brinister at yahoo dot com>

pkgname=python-cheetah3
_name=Cheetah3
pkgver=3.2.5
pkgrel=4
pkgdesc="A Python powered template engine and code generator"
arch=(any)
url="http://www.cheetahtemplate.org"
license=(MIT)
makedepends=('python-setuptools')
source=("https://files.pythonhosted.org/packages/source/${_name::1}/${_name}/${_name}-${pkgver}.tar.gz")
sha512sums=('1431095b0027ec5789bf6ce9488587b599c42f394e3f1f8c53a3c37efc3f0052580e3b1e00cf5f5f682ed5b37ec3eac35f5b578c05d64e2b9592385fd089aabe')

package() {
  optdepends=('python-markdown')

  cd "${srcdir}/${_name}-${pkgver}"
  python setup.py install --root="${pkgdir}" --optimize=1
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

