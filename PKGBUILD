# Maintainer: Mathieu Clabaut <mathieu.clabaut@gmail.com>

pkgname=diff-pdf-svn
pkgver=20140820
pkgrel=3
pkgdesc="Tool for visually comparing two PDF files"
url="https://github.com/vslavik/diff-pdf"
license=('GPL')
arch=(i686 x86_64)

depends=(poppler-qt wxgtk)
source=('diff-pdf::svn+https://github.com/vslavik/diff-pdf.git/trunk#revision=HEAD')
md5sums=('SKIP')


build () {
   cd "$srcdir/diff-pdf"
   pwd
   ./bootstrap
   ./configure --prefix=/usr
   make || return 1
}

package() {
    cd "$srcdir/diff-pdf"
    make DESTDIR="$pkgdir" install || return 1
}
