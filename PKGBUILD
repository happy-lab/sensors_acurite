#
# This is the PKGBUILD for AcuRite Sensors MQTT Package
#

pkgname=sensors_acurite
pkgver=1.1.0
pkgrel=1
pkgdesc="AcuRite Weather Station Sensors Publish Through MQTT"
arch=('i686' 'x86_64' 'arm' 'armv6h' 'armv7h')
url="http://happy-lab.llc/"
depends=('python')
provides=('sensors_acurite')
license=('MIT')
source=("$pkgname" "$pkgname.service" "$pkgname.conf.example" "LICENSE")
install=$pkgname.install
sha256sums=('7e4dc5e10b8ab837b3646677712deefc88992142713f14f9bdb0393f43d6f63d'
            'ee7df605e53c7755aecd017163e1c59f8fd16e06ba683f22869c4c669f0fd820'
            'fabeb2b9f6291920153ac1cdadd0bc5c72daa1fd6ab459e945fedb457d8e1f76'
            'c5089bc858e3308732e9e9a0ddeb1ad36a77d628150c038ebcdf54027208218a')

package() {

  # Daemon
  install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname"

  # Daemon systemd service file
  install -Dm644 "$pkgname.service" "$pkgdir/usr/lib/systemd/system/$pkgname.service"

  # Daemon configuration file
  install -Dm644 "$pkgname.conf.example" "$pkgdir/etc/sensors/$pkgname.conf.example"

  # Daemon PID file
  #echo 'pid_file /run/$pkgname.pid' >> "$pkgdir/etc/sensors/$pkgname.conf.example"

  # License
  install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"

}
