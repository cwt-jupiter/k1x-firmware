# Maintainer: Chaiwat Suttipongsakul <cwt@bashell.com>

pkgname=k1x-firmware
pkgdesc="Firmware for SpacemiT K1-x boards"
pkgver=2.0.4
pkgrel=1
arch=('riscv64')
url="https://gitee.com/bianbu-linux/buildroot-ext"
license=('other')
_tag=v${pkgver}
_srcname=buildroot-ext-${_tag}
#options=('!debug')
source=("${_srcname}.tar.gz::${url}/repository/archive/${_tag}.tar.gz"
        'k1x-esos.conf')

b2sums=('7b974b2d4fb56c130fc26c52c1c12a8fe8a2ffe2b5d165166f22844f6139b825b526e1ceac6ad55783c255a6d0729eb5dbdbe239288f7617cc02865821d255de'
        '41a4933db5dda9dd2501c502f8dd51f6141a0d54c214fd80458770fd62730eac72fffe33e13c4de0cb1c90614bf9eae1addf515a11cf66f1e72e9a701905087f')

package() {
    mkdir -p ${pkgdir}/usr/lib/firmware
    cd ${_srcname}/board/spacemit/k1/target_overlay/lib/firmware
    cp -a * ${pkgdir}/usr/lib/firmware/
    install -Dm644 ${srcdir}/k1x-esos.conf ${pkgdir}/etc/mkinitcpio.conf.d/k1x-esos.conf
}

