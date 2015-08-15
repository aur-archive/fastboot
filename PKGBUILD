# Maintainer: Muflone http://url.muflone.com/contacts
# Contributor: Marco A Rojas <marquicus[at]gmail.com>

pkgname=fastboot
pkgver=20090426
pkgrel=5
pkgdesc="Tool used to flash the filesystem in Android devices from a host via USB"
arch=("i686" "x86_64")
license=('custom')
url="http://www.htcdev.com/process/legal_fastboot_linux"
depends=('libusb' 'gcc-libs')
[[ $CARCH = x86_64 ]] && depends[1]='lib32-gcc-libs'
optdepends=('android-udev: Udev rules to connect Android devices to your linux box'
            'android-sdk-platform-tools: Platform-Tools for Google Android SDK (adb, aapt, aidl, dexdump and dx')
source=("http://dl4.htc.com/RomCode/ADP/fastboot.zip"
        "LICENSE")
sha1sums=('a2cdd68ae99738cad0db1e88e63199befd1b13f2'
          'fc4e5481283ff5e9d74296a7267439220b2a5c7e')
DLAGENTS="http::/usr/bin/curl -O --referer ${url} %u"

package() {
  install -D -m755 "${srcdir}/${pkgname}" "$pkgdir/usr/bin/${pkgname}"
  install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
