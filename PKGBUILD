# Maintainer: Alad Wenter <alad AT linuxbbq DOT org>

pkgname=spacefm-plugin-corbeille
pkgver=1.0.7
pkgrel=2
pkgdesc="a trash plugin compliant with the FreeDesktop.org Trash specification."
arch=('any')
url="https://github.com/IgnorantGuru/spacefm/wiki/plugins"
license=('GPL3')
depends=('spacefm')
source=(https://gitorious.org/projets-divers/corbeille-spacefm/archive/master.zip)
sha256sums=('e6615fc8a24c1f2bde0ab51d36346a131f65f22d1b697e31ddcc955347e3eb3b')
_lang=en
_dir="Corbeille-$_lang-source"

prepare() {
	cd "$srcdir/projets-divers-corbeille-spacefm"
	./script.sh archive "$_lang"
	mkdir -p "$_dir"
	tar -xf "$_dir".spacefm-plugin.tar.gz -C "$_dir"
}

package() {
	cd "$srcdir/projets-divers-corbeille-spacefm"
	mkdir -p "$pkgdir/usr/share/spacefm/plugins"
	cp -ar "$_dir" "$pkgdir/usr/share/spacefm/plugins/$_dir"
}

