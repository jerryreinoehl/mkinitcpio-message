# Maintainer: Jerry Reinoehl <jerryreinoehl@gmail.com>
pkgname=mkinitcpio-message
pkgver=1.0.0
pkgrel=1
pkgdesc="mkinitcpio hook to display a message"
arch=(any)
url="https://github.com/jerryreinoehl/mkinitcpio-message"
license=('GPL')
depends=(mkinitcpio)

package() {
  mkdir -p $pkgdir/usr/lib/initcpio/{hooks,install}

  echo startdir $startdir

  install -o root -g root -m 0644 \
    $startdir/install/message \
    $pkgdir/usr/lib/initcpio/install/message

  install -o root -g root -m 0644 \
    $startdir/hooks/message \
    $pkgdir/usr/lib/initcpio/hooks/message
}
