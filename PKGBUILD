pkgname=aster-keyring
pkgver=20240710
pkgrel=1
pkgdesc="Aster keyring"
arch=('any')
url="https://github.com/sahanuser/Aster-Linux-ISO"
license=('GPL')
install="${pkgname}.install"
source=('Makefile'
        'aster.gpg'
	'aster-revoked'
	'aster-trusted')
validpgpkeys=('DCB6D09D1EEB4C76EFEDC65AEF8B1E906442569F')
pkgver() {
  date +%Y%m%d
}
md5sums=('e32abc16b1d41dfcd6cb77baece98321'
         'e32b6febe9d24c80040a6f59ca208f31'
         'd41d8cd98f00b204e9800998ecf8427e'
         '55279b022ef37d56408a4573a2049094')
package() {
	cd "${srcdir}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
