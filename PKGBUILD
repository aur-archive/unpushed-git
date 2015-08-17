# Maintainer: Axper Jan <483ken 4t gma1l

pkgname=unpushed-git
pkgver=v1.1.0.r1.g1f8f572
pkgrel=1
pkgdesc="Tool to scan a filesystem for uncommitted and unpushed version control changes"
arch=('any')
url="https://github.com/nailgun/unpushed"
license=('MIT')
depends=('python2')
makedepends=('git')
source=("git+https://github.com/nailgun/unpushed.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/unpushed"
  git describe --long | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "unpushed"
  python2 setup.py install --root="$pkgdir/" --optimize=1
  install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/unpushed-git/LICENSE"
}

# vim:set ts=2 sw=2 et:
