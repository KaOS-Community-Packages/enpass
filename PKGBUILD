pkgname='enpass'
pkgver=5.6.9
pkgrel=1
pkgdesc='Password manager for iOS, Android, Windows, Linux, Mac'
arch=('x86_64')
url='http://enpass.io/'
license=('custom')
depends=('libxss' 'lsof')
options=('!strip')
source=("http://repo.sinew.in/pool/main/e/enpass/${pkgname}_${pkgver}_amd64.deb")
md5sums=('f783c2c5df5afb2b0ae47359307d2870')

package() {
    tar xfz ${srcdir}/data.tar.gz -C ${pkgdir}

    chmod 755 ${pkgdir}/opt/
    find ${pkgdir}/usr/ -type d -exec chmod 755 {} \;

    mkdir -p ${pkgdir}/usr/bin
    ln -s /opt/Enpass/bin/runenpass.sh ${pkgdir}/usr/bin/enpass
}
