# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# See http://wiki.archlinux.org/index.php/VCS_PKGBUILD_Guidelines
# for more information on packaging from GIT sources.

# Maintainer: Your Name <youremail@domain.com>
pkgname=kate-syntax-markdown-git
pkgver=VERSION
pkgrel=1
pkgdesc="Markdown syntax highlighting for the KDE Kate Advanced Editor."
arch=()
url="https://github.com/treeofsephiroth/kate-markdown"
license=('GPL')
groups=()
depends=('kdesdk-kate')
makedepends=('git')
noextract=()
#md5sums=() #generate with 'makepkg -g'

_gitroot=git://github.com/treeofsephiroth/kate-markdown.git
_gitname=kate-markdown

build() {
  cd "$srcdir"
  msg "Connecting to GIT server...."

  if [[ -d "$_gitname" ]]; then
    cd "$_gitname" && git pull origin
    msg "The local files are updated."
  else
    git clone "$_gitroot" "$_gitname"
  fi

  msg "GIT checkout done or server timeout"
  msg "Starting build..."

  rm -rf "$srcdir/$_gitname-build"
  git clone "$srcdir/$_gitname" "$srcdir/$_gitname-build"
  cd "$srcdir/$_gitname-build"

}

package() {
  cd "$srcdir/$_gitname-build"
  cp markdown.xml $pkgdir/usr/share/apps/katepart/syntax/markdown.xml
}

# vim:set ts=2 sw=2 et: