# Maintainer: kevku <kevku@gmx.com>
pkgname=python2-tesseract-svn
pkgver=660
pkgrel=2
pkgdesc="python wrapper class for tesseract OCR"
arch=('x86_64' 'i686')
url="https://code.google.com/p/python-tesseract/"
license=('GPL3')
depends=('python2' 'opencv' 'tesseract')
makedepends=('swig' 'python2-distribute')
provides=('python2-tesseract')
source=("python2-tesseract::svn+https://python-tesseract.googlecode.com/svn/trunk/")
sha256sums=('SKIP')

pkgver() {
    cd "$srcdir/python2-tesseract"
    svnversion | tr -d [A-z]
}

prepare() {
    cd "$srcdir/python2-tesseract"
    #cp saved4Tesseract301/tprintf.h .
}

build() {
    cd "$srcdir/python2-tesseract"
    python2 setup.py build
  
}

package(){
    cd "$srcdir/python2-tesseract"
    python2 setup.py install --root="$pkgdir/" --optimize=1
}

# vim:set ts=2 sw=2 et:
