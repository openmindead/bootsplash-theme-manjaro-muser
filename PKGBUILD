# Maintainer: Vladimir Yerilov <openmindead AT gmail DOT com>
pkgbase=bootsplash-themes
pkgname=('bootsplash-theme-manjaro-muser')
pkgver=0.1
pkgrel=4
url="https://github.com/openmindead/bootsplash-theme-manjaro-muser"
arch=('x86_64')
license=('GPL')

depends=('systemd')
builddepends=('imagemagick')
optdepends=('bootsplash-systemd: for better interration of bootsplash')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-theme-manjaro-muser.sh'
	'bootsplash-theme-manjaro-muser.initcpio_install'
	'spinner.gif'
	'no.png')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

build() {
  cd "$srcdir"
  sh ./bootsplash-theme-manjaro-muser.sh
}

package_bootsplash-theme-manjaro-muser() {
  pkgdesc="'Manjaro' branded Bootsplash Theme for Manjaro Linux"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-theme-manjaro-muser" "$pkgdir/usr/lib/firmware/bootsplash-themes/manjaro-muser/bootsplash"
  install -Dm644 "$srcdir/bootsplash-theme-manjaro-muser.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-theme-manjaro-muser"
} 
