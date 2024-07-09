pkgname=aster-keyring
pkgver=20240710
pkgrel=1
pkgdesc="Aster keyring"
arch=('x86_64')
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
         '9771285fb7d07d03fcbcc8b580b68cd7'
         'd41d8cd98f00b204e9800998ecf8427e'
         '6db6db855a6eee893898974811a591dd')
package() {
	cd "${srcdir}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
