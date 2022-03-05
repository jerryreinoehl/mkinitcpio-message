# Maintainer: Jerry Reinoehl <jerryreinoehl@gmail.com>
pkgname=mkinitcpio-message
pkgver=1.0.0
pkgrel=1
pkgdesc="mkinitcpio hook to display a message"
arch=(any)
url="https://github.com/jerryreinoehl/mkinitcpio-message"
license=('GPL')
install=mkinitcpio-message.install
depends=(mkinitcpio)

package() {
  install -D -m 0644 \
    "$startdir/install/message" \
    "$pkgdir/usr/lib/initcpio/install/message"

  install -D -m 0644 \
    "$startdir/hooks/message" \
    "$pkgdir/usr/lib/initcpio/hooks/message"
}
