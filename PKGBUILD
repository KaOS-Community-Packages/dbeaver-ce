pkgname=dbeaver-ce
pkgver=23.1.0
pkgrel=1
pkgdesc="Free Universal Database Tool"
arch=('x86_64')
depends=('openjdk')
url="https://dbeaver.io/"
license=('Apache')
source=("https://github.com/dbeaver/dbeaver/releases/download/${pkgver}/${pkgname}-${pkgver}-linux.gtk.x86_64.tar.gz")
md5sums=('4dca8ab92513523b2c8df2c85aa47ff9')

package() {
    cd "${srcdir}"
    install -dm755 "${pkgdir}/usr/share/applications"
    install -dm755 "${pkgdir}/usr/bin"
    cp --preserve=mode -r "dbeaver" "${pkgdir}/usr/share/${pkgname}"
        
    ln -sf /usr/share/${pkgname}/dbeaver ${pkgdir}/usr/bin/${pkgname}
    ln -sf /usr/share/${pkgname}/${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
}

