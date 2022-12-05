# Maintainer: Kawaki <rtkay123@hotmail.com>
pkgname=otf-dank-mono
pkgver=r1.2b88f11
pkgrel=1
epoch=
pkgdesc="A cool monospace font with ligatures"
arch=('any')
url="https://dank.sh"
license=('Commercial')
makedepends=('git')
optdepends=('ttf-nerd-fonts-symbols-1000-em-mono: nerd font symbols support')
source=('otf-dank-mono::git+ssh://git@github.com/kawaki-san/dank-mono.git')
md5sums=('SKIP')

pkgver() {
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  find . -iname "*.otf" -execdir install -Dm644 {} "$pkgdir/usr/share/fonts/TTF/{}" \;
}
