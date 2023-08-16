pkgname=docker-shell
pkgver=v0.2.0.r0.g5018c2e  # You can adjust this as per the actual version of your software
pkgrel=1
pkgdesc="A tool to run a Docker container with system volumes mounted"
arch=('i686' 'x86_64')  # Adjust as needed based on which architectures your software supports
url="https://github.com/ncsa/docker-shell"  # Replace with the actual URL of your repository
license=('MIT')  # Adjust as needed based on the license of your software
makedepends=('go')
source=("git+$url.git")  # Get source code from git
sha256sums=('SKIP')  # You can replace SKIP with the actual sha256sum or use a tool to compute it

pkgver() {
    cd "$pkgname"
    # This uses git to get the latest tag. If tags are not being used, you might need a different command.
    git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

build() {
    cd "$pkgname"
    make
}

package() {
    cd "$pkgname"
    make PREFIX="$pkgdir/usr" install
}
