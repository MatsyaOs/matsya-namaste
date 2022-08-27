pkgname=matsya-namaste-git
_pkgname=matsya-namaste
pkgver=22.10
pkgrel=06
pkgdesc=" Welcome Application for Matsya Os"
arch=('x86_64')
url="https://github.com/matsyaos/${_pkgname}"
license=('GPL')
depends=('git')
provides=('matsya-namaste')
source=("git+${url}.git")
destdir="/usr/share/matsya"
destdir_desktop="/etc/xdg/autostart"
destdir_icon="/usr/share/icons/hicolor/64x64/apps"
md5sums=('SKIP')

package() {
    cd "${_pkgname}"
    mkdir -p "${pkgdir}"/{"${destdir}","${destdir_desktop}","${destdir_icon}"}
    mkdir -p "${pkgdir}"/usr/share/applications
    cp -r ./data/. "${pkgdir}${destdir}"
    cp ./data/Welcome.desktop "${pkgdir}${destdir_desktop}"
    cp ./data/Welcome.desktop "${pkgdir}"/usr/share/applications
    install -Dm644  ./data/amos.png "${pkgdir}${destdir_icon}"
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${_pkgname}/LICENSE"
    install -Dm644 README.md "${pkgdir}/usr/share/doc/${_pkgname}/README.md"
}
