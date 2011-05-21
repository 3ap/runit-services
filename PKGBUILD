# Contributor: Kevin Berry <kb@rubyists.com>
# Maintainer: TJ Vanderpoel <tj@rubyists.com>
pkgname='runit-services'
pkgver=1.0.0
pkgrel=4
arch=('x86_64' 'i686')
pkgdesc="A collection of commonly used service directories"
url="http://github.com/rubyists/runit-services"
license=('custom')
provides=('runit-services')
conflicts=('runit-services-git')
depends=('runit-dietlibc')
makedepends=('git')
backup=('etc/sv/apache2/log/run' 'etc/sv/apache2/run' 'etc/sv/avahi/log/run' 'etc/sv/avahi/run' 'etc/sv/couchdb/log/run' 'etc/sv/couchdb/run' 'etc/sv/cups/log/run' 'etc/sv/cups/run' 'etc/sv/dbus/log/run' 'etc/sv/dbus/run' 'etc/sv/freeswitch/log/run' 'etc/sv/freeswitch/run' 'etc/sv/gdm/run' 'etc/sv/kdm/run' 'etc/sv/lighttpd2/log/run' 'etc/sv/lighttpd2/run' 'etc/sv/mysql/log/run' 'etc/sv/mysql/run' 'etc/sv/ntpd/log/run' 'etc/sv/ntpd/run' 'etc/sv/openntpd/log/run' 'etc/sv/openntpd/run' 'etc/sv/openvpn/log/run' 'etc/sv/openvpn/run' 'etc/sv/postgresql/log/run' 'etc/sv/postgresql/run' 'etc/sv/sshd/log/run' 'etc/sv/sshd/run')
source=("https://download.github.com/rubyists-runit-services-1.0.0-0-g3186b6c.tar.gz")
md5sums=('64e3e1216f53257c31fb35aad8bb4266')

package() {
  cd "$srcdir/rubyists-runit-services-3186b6c/"
  install -D -m 0644 COPYRIGHT "$pkgdir/usr/share/doc/runit-services/COPYRIGHT"
  install -D -m 0644 README.md "$pkgdir/usr/share/doc/runit-services/README.md"
  install -D -d "$pkgdir/etc/sv"
  for service in etc/sv/*;do
    cp -a $service "$pkgdir/etc/sv/"
  done
}
