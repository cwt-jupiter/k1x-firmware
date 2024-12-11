# Maintainer: Chaiwat Suttipongsakul <cwt@bashell.com>

pkgname=k1x-firmware
pkgdesc="Firmware for SpacemiT K1-x from Bianbu buildroot-ext"
pkgver=2.0.2
pkgrel=1
arch=('riscv64')
url="https://gitee.com/bianbu-linux/buildroot-ext"
license=('other')
_tag=v${pkgver}
_srcname=buildroot-ext-${_tag}
#options=('!debug')
source=("${_srcname}.tar.gz::${url}/repository/archive/${_tag}.tar.gz")

b2sums=('5c1e931eff2ee74fc58785a73e684867a15bc7eccf029bada7b9a380f770a40b5e484e567ee88e579b81a25e0106872a5cb5845f30c259684c959b4760213730')

package() {
    mkdir -p ${pkgdir}/usr/lib/firmware
    cd ${_srcname}/board/spacemit/k1/target_overlay/lib/firmware
    cp -a * ${pkgdir}/usr/lib/firmware/
}

