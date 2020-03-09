#
# This is the PKGBUILD for AcuRite Sensors MQTT Package
#

pkgname=sensors_acurite
pkgver=1.1.0
pkgrel=1
pkgdesc='AcuRite Weather Station Sensors Publish Through MQTT'
arch=('i686' 'x86_64' 'arm' 'armv6h' 'armv7h')
url='http://happy-lab.llc/'
depends=('python')
provides=('sensors_acurite')
license=('MIT')
source=('sensors_acurited' 'sensors_acurite.service' 'sensors_acurite.conf.example' 'LICENSE')
install=$pkgname.install
sha256sums=('926d07fcd2794f64a14bc1059128830d4e96432b18485ee06b21f4dc72983bb3'
            '64ddd7d26d36f9f6cc16f21cc3f7d817d3e393c96ceedae0ea231a0c7dec9b7d'
            'e72ffdfc10756ccc189d74b50e2ddaab049a45a0c3f0d96ce2a642787e4aeb37'
	    '8c75a9231db8906865e29706ed63aad18fd918c92c15dbefbb13c25fe42850b4')

package() {

  # Daemon
  install -Dm755 "sensors_acurited" "${pkgdir}/usr/bin/sensors_acurited"

  # Daemon systemd service file
  install -Dm644 "sensors_acurite.service" "${pkgdir}/usr/lib/systemd/system/sensors_acurite.service"

  # Daemon configuration file
  install -Dm644 "sensors_acurite.conf.example" "${pkgdir}/etc/sensors/sensors_acurite.conf.example"

  # Daemon PID file
  #echo 'pid_file /run/sensors_acurite.pid' >> "${pkgdir}/etc/sensors/sensors_acurite.conf.example"

  # License
  install -Dm644 "LICENSE" "${pkgdir}/usr/share/licenses/sensors_acurite/LICENSE"

}
