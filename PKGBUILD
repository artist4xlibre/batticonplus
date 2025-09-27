# Maintainer: artist for Artix Linux

pkgbase=batticonplus
pkgname=(batticonplus batticonplus-ayatana)
pkgver=2.0.0
pkgrel=1
pkgdesc='Lightweight battery icon for the system tray (based on cbatticon)'
arch=(x86_64)
url='https://github.com/artist'
license=(GPL2)
depends=(libnotify gtk3)
makedepends=(libayatana-appindicator-glib)
provides=(cbatticon)
conflicts=(cbatticon)
replaces=(cbatticon)
#source=("git+$url#commit=2b87a0f033a6cd173fa59174b921cf5d231771b6")
source=(batticonplus.zip)
b2sums=('25889a67b9ebd1c98946747e74cfbee0857a25406dce71234e4b41fd718f5ac01d7c98d48336aa83301fa542de03359409493f34be59207dcde1bb06b89b9128')

package_batticonplus() {
  make -C $pkgname WITH_NOTIFY=1 WITH_GTK3=1 WITH_APPINDICATOR=0 PREFIX="$pkgdir/usr" install
  cd "$srcdir/$pkgname"
  install -D -m644 -t "$pkgdir/usr/share/doc/$pkgname/" Changelog
  install -D -m644 -t "$pkgdir/usr/share/licenses/$pkgname/" COPYING
}

package_batticonplus-ayatana() {
  pkgdesc='Lightweight battery icon for the system tray (fork of cbatticon), better for Wayland'
  depends+=(libayatana-appindicator)
  make -B -C $pkgbase WITH_NOTIFY=1 WITH_GTK3=1 WITH_APPINDICATOR=1 PREFIX="$pkgdir/usr" install
  cd "$srcdir/$pkgbase"
  install -D -m644 -t "$pkgdir/usr/share/doc/$pkgbase/" Changelog
  install -D -m644 -t "$pkgdir/usr/share/licenses/$pkgbase/" COPYING
}

