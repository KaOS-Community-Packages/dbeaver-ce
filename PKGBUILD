pkgname=dbeaver-ce
pkgver=22.2.4
pkgrel=1
pkgdesc="Free Universal Database Tool"
arch=('x86_64')
depends=('openjdk')
url="https://dbeaver.io/"
license=('Apache')
source=("https://github.com/dbeaver/dbeaver/releases/download/${pkgver}/${pkgname}-${pkgver}-linux.gtk.x86_64.tar.gz")
md5sums=('680b5a3144bc1f92694507f8cf1275cb')

package() {
    cd "${srcdir}"
    install -dm755 "${pkgdir}/usr/share/applications"
    install -dm755 "${pkgdir}/usr/bin"
    cp --preserve=mode -r "dbeaver" "${pkgdir}/usr/share/${pkgname}"
        
    ln -sf /usr/share/${pkgname}/dbeaver ${pkgdir}/usr/bin/${pkgname}
    ln -sf /usr/share/${pkgname}/${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
}

