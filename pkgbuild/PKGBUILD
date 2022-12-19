pkgname=lxdm-biglinux-theme
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
pkgdesc='BigLinux Lightweight X11 Display Manager'
arch=('any')
url="https://github.com/biglinux/$pkgname"
license=('GPL3')
depends=('lxdm')
provides=("$pkgname")
# conflicts=('')
source=("git+${url}.git")
md5sums=('SKIP')
if [ -e "${pkgname}.install" ];then
    install=${pkgname}.install
fi


package() {

    InternalDir="${srcdir}/${pkgname}"

    # Copy files
    if [ -d "${InternalDir}/usr" ]; then
        cp -r "${InternalDir}/usr" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/etc" ]; then
        cp -r "${InternalDir}/etc" "${pkgdir}/"
    fi

    if [ -d "${InternalDir}/opt" ]; then
        cp -r "${InternalDir}/opt" "${pkgdir}/"
    fi

}
