pkgname=dbeaver-ce
_pkgname=dbeaver
pkgver=7.3.1
pkgrel=2
pkgdesc="Free Universal Database Tool"
arch=('x86_64')
depends=('openjdk')
url="https://dbeaver.io/"
license=('Apache')
source=("https://github.com/dbeaver/dbeaver/releases/download/${pkgver}/${pkgname}-${pkgver}-linux.gtk.x86_64.tar.gz")
md5sums=('d395c01267a531bedf9816cf8715ed25')

package() {
    cd "${srcdir}"
    rm -rf dbeaver/jre
    install -dm755 "${pkgdir}/usr/share/applications"
    install -dm755 "${pkgdir}/usr/bin"
    cp --preserve=mode -r "dbeaver" "${pkgdir}/usr/share/dbeaver"
        
    ln -sf /usr/share/${_pkgname} ${pkgdir}/usr/bin/${_pkgname}
    ln -sf /usr/share/${_pkgname}/${_pkgname}.desktop ${pkgdir}/usr/share/applications/${_pkgname}.desktop
}

