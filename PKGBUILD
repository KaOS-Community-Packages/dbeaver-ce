pkgname=dbeaver-ce
_pkgname=dbeaver
pkgver=21.1.0
pkgrel=1
pkgdesc="Free Universal Database Tool"
arch=('x86_64')
depends=('openjdk')
url="https://dbeaver.io/"
license=('Apache')
source=("https://github.com/dbeaver/dbeaver/releases/download/${pkgver}/${pkgname}-${pkgver}-linux.gtk.x86_64.tar.gz")
md5sums=('12ba074d5f10e13e3caa7c7e5a7ecb7f')

package() {
    cd "${srcdir}"
    install -dm755 "${pkgdir}/usr/share/applications"
    install -dm755 "${pkgdir}/usr/bin"
    cp --preserve=mode -r "dbeaver" "${pkgdir}/usr/share/dbeaver"
        
    ln -sf /usr/share/${_pkgname} ${pkgdir}/usr/bin/${_pkgname}
    ln -sf /usr/share/${_pkgname}/${_pkgname}.desktop ${pkgdir}/usr/share/applications/${_pkgname}.desktop
}

