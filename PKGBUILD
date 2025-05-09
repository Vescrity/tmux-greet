# Maintainer: Vescrity
pkgname=tmux-greet-git
pkgver="0"
pkgrel=1
epoch=1
pkgdesc='Launch tuigreet in tmux.'
arch=(any)
depends=(
    tmux
    greetd-tuigreet
)
optdepends=(
)
makedepends=(
  git
)
provides=(tmux-greet greetd-agreety) # I just don't want to install it since I have one greeter.
conflicts=(tmux-greet)
source=('git+https://github.com/Vescrity/tmux-greet')
sha256sums=('SKIP')
backup=(etc/tmux-greet/tmux-greet-startup)
pkgver() {
    cd "$srcdir/tmux-greet"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short=7 HEAD)"
}
package() {
  cd "$srcdir/tmux-greet"
  install -d "${pkgdir}/usr/bin"
  install -Dm755 "tmux-greet" "${pkgdir}/usr/bin/tmux-greet"
  install -d "${pkgdir}/etc/tmux-greet"
  install -Dm755 "tmux-greet-startup" "${pkgdir}/etc/tmux-greet/tmux-greet-startup"
}
