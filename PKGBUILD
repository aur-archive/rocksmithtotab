# Maintainer: Jefferson Gonzalez <jgmdev@gmail.com>

pkgname=rocksmithtotab
pkgver=0.9.9
pkgrel=1
_extname=RocksmithToTab

pkgdesc="Exports Rocksmith 2014 arrangements to Guitar Pro or TuxGuitar tabs."
url="http://www.rocksmithtotab.de/"
arch=('any')
license=('MIT')
depends=('mono')

source=(
  "http://sourceforge.net/projects/rocksmithtotab/files/Releases/RocksmithToTab_v$pkgver.tar.gz"
  "rocksmithtotab"
  "rocksmithtotab-gui"
  "logo.png"
  "rocksmithtotab.desktop"
)

sha256sums=(
  'db16d1e3cd87e6a593b79504c648b8f4702315ffc6b595b80a7d583be02a89fe'
  '4bab67070a183b4d6c8cd0aef4d8f6908008d3b29187bb79abcc208e134fa684'
  'cdeb75e502287db060a7b43974d41735a30e953dc23ffa35f5218d7f6d3f2cd2'
  'b1d4c20e0d76c29074614eefd809e0c65edcdc49eaa5b996113216d67803a2f4'
  '63e54d199d3e15c0919d1aca25fa9ad5d0497af81edd69f01392fbb437dafdf3'
)

package() {
  cd ..
  install -d -m755 -p "$pkgdir"/usr/bin
  install -d -m755 -p "$pkgdir"/usr/lib/"$pkgname"
  install -d -m755 -p "$pkgdir"/usr/share/applications
  install -m755 rocksmithtotab "$pkgdir"/usr/bin/
  install -m755 rocksmithtotab-gui "$pkgdir"/usr/bin/
  cp -ar src/"$_extname"/* "$pkgdir"/usr/lib/"$pkgname"
  install -m644 logo.png "$pkgdir"/usr/lib/"$pkgname"
  install -m644 rocksmithtotab.desktop "$pkgdir"/usr/share/applications
}
# vim:set ts=2 sw=2 et:
