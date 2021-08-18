# Maintainer:  chocotan < loli at linux.com>

pkgname='java-11-dragonwell'
pkgver='11.0.12.8'; _build='11'; _hash='f411702ca7704a54a79ead0c2e0942a3';
_major="${pkgver%%.*}"
_jdkdir='/usr/lib/jvm'
pkgrel='1'
pkgdesc="Alibaba Java ${_major} Development Kit"
arch=('x86_64')
url='http://dragonwell-jdk.io/'
license=('custom')
depends=('java-runtime-common>=3')
provides=(
  "java-environment=${_major}"
  "java-environment-jdk=${_major}"
  "jdk=${pkgver}"
)
source=(
  "https://github.com/alibaba/dragonwell11/releases/download/${pkgver}-GA/Alibaba_Dragonwell_${pkgver}_x64_linux.tar.gz"
)

md5sums=('6aaf8354662240a1d4a8e66baf2c1b4d')
sha256sums=('045166d6dee2e55e2571bb9c02dcf822b538d44a9b5aaac918032e8e137ca512')

package() {
    # Install
    install -d "${pkgdir}/${_jdkdir}/${pkgname}"
    cd "${srcdir}/jdk-11.0.12.8+0"
    cp -a lib jmods man bin include legal conf release "${pkgdir}/${_jdkdir}/${pkgname}/"
}
