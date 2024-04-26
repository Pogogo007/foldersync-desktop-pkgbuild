#Maintainer Nekoh
pkgname="foldersync-desktop"
pkgver=1.2.0
pkgrel=1
pkgdesc="Advanced syncing tool for Windows, Linux and MacOS"
arch=('x86_64')
url="https://foldersync.io/desktop/"
license=('custom')
conflicts=('foldersync-desktop')
depends=('fuse2' 'libxi' 'libxrender' 'libxtst' 'mesa-utils' 'fontconfig' 'gtk3')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/tacitdynamics/foldersync-desktop-production/releases/download/${pkgver}/foldersync-desktop-${pkgver}-linux-amd64.tar.gz")
sha512sums=('da25b2d56e6a173dce39d08579476ccec65159b6c5d7cc70f456243cfaba450456e56be9414279af93ea6d2c0b83aff276e9cefaff0c99a5f268c1071b292161')

package() {
    mkdir -p "${pkgdir}/usr/lib/tacit-dynamics-aps/foldersync-desktop/"
    mkdir -p "${pkgdir}/usr/bin"
    cp -a "${srcdir}/foldersync-desktop-${pkgver}/share" "${pkgdir}/usr/"
    cp -a "${srcdir}/foldersync-desktop-${pkgver}/bin" "${pkgdir}/usr/lib/tacit-dynamics-aps/foldersync-desktop/"
    cp -a "${srcdir}/foldersync-desktop-${pkgver}/lib" "${pkgdir}/usr/lib/tacit-dynamics-aps/foldersync-desktop/"
    ln -s "/usr/lib/tacit-dynamics-aps/foldersync-desktop/bin/foldersync-desktop" "${pkgdir}/usr/bin/foldersync-desktop"
}
