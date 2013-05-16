# Maintainer: Laurie Clark-Michalek <bluepeppers@archlinux.us>

pkgname=archey3
pkgver=0.4
pkgrel=1
pkgdesc="Python script to display system infomation alongside the Arch Linux logo."
arch=('any')
url="http://bluepeppers.github.com/archey3"
license=('GPL')
depends=('python')
makedepends=('python-distribute')
optdepends=(
'python3-mpd-git: python mpd libary for mpd protocol (optional, mpc can be used instead)'
'python-logbook-git: for logging'
'imagemagick: for default screenshot command'
)
conflicts=('archey')
provides=('archey')
source=("https://github.com/bluepeppers/${pkgname}/archive/${pkgname}-${pkgver}.tar.gz")
sha256sums=('bef444085c265f34b9cf169baba7c755e4fba8858ba5011c970a89c58c4119df')

package() {
	cd "${pkgname}-${pkgver}"
	python setup.py install --root=${pkgdir}
	install -D -m644 COPYING ${pkgdir}/usr/share/licenses/archey/COPYING
	
	# Comment line below to install side by side with standard archey
	ln -s /usr/bin/archey3 ${pkgdir}/usr/bin/archey
} 
