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
sha256sums=('5c6896328422b792b28acfb488aee71ef8ead3c4f565bb9a74ba9960fbad2d22'
            'bfa543057556d1d8ef30612c248b65344009460958f2c22e15d97299a16eb01e'
            'e72ffdfc10756ccc189d74b50e2ddaab049a45a0c3f0d96ce2a642787e4aeb37'
	    '8c75a9231db8906865e29706ed63aad18fd918c92c15dbefbb13c25fe42850b4')

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
