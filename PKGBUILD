# Maintainer: Michael DeGuzis <mdeguzis@gmail.com>

pkgname=xenia-git
_gitname=xenia
pkgver=1.0.119.r402.gbc0ddbb
pkgrel=1
pkgdesc='Experimental emulator for the Xbox 360'
url='https://github.com/benvanik/xenia'
arch=('any')
license=('custom:Ben Vanik')
conflicts=('xenia')
provides=('xenia')
depends=('')
makedepends=('clang' 'git' 'llvm' 'lua' 'python2'
	     'premake-git' 'python2-pexpect')
source=('git+https://github.com/benvanik/xenia.git')
md5sums=('SKIP')

pkgver() {

    cd ${_gitname}
    git describe --tags --long | sed -r -e 's,^[^0-9]*,,;s,([^-]*-g),r\1,;s,[-_],.,g'

}

build() {

  cd ${srcdir}/${_gitname}
  python2 xenia-build lint --all
  python2 xenia-build setup
  CC="/usr/bin/clang" CXX="/usr/bin/clang++" python2 xenia-build build  

}

package() {

  cd ${pkgname%-git}
  cp to do

}
