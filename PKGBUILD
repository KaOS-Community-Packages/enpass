pkgname='enpass'
pkgver=6.5.1.723
pkgrel=1
pkgdesc='Password manager for iOS, Android, Windows, Linux, Mac'
arch=('x86_64')
url='http://www.enpass.io/'
license=('custom')
depends=('libxss' 'lsof' 'curl')
options=('!strip')
source=("http://repo.sinew.in/pool/main/e/enpass/${pkgname}_${pkgver}_amd64.deb")
sha512sums=('ce16a13a8f0b8e20fc987924f5d2540bd39e8f9fc6405720f6a90a504b94b47e9747a8b0c46636ad670eba066344ac088a38acf27c70874248d582688560fc9c')

package() {
    tar xfz ${srcdir}/data.tar.gz -C ${pkgdir}

    chmod 755 ${pkgdir}/opt/
    find ${pkgdir}/usr/ -type d -exec chmod 755 {} \;

    mkdir -p ${pkgdir}/usr/bin
    ln -s /opt/Enpass/bin/runenpass.sh ${pkgdir}/usr/bin/enpass
}
