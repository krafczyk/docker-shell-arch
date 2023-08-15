pkgname=docker-shell
pkgver=0.1.0  # You can adjust this as per the actual version of your software
pkgrel=1
pkgdesc="A tool to run a Docker container with system volumes mounted"
arch=('i686' 'x86_64')  # Adjust as needed based on which architectures your software supports
url="https://github.com/ncsa/docker-shell"  # Replace with the actual URL of your repository
license=('MIT')  # Adjust as needed based on the license of your software
makedepends=('go')
source=("$url/archive/v$pkgver.tar.gz")  # Assumes tags are used for versioning
sha256sums=('SKIP')  # You can replace SKIP with the actual sha256sum or use a tool to compute it

build() {
    cd "$pkgname-$pkgver"
    make
}

package() {
    cd "$pkgname-$pkgver"
    make PREFIX="$pkgdir/usr/bin" install
}
