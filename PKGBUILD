# Maintainer: @zstg <zestig@duck.com>
pkgname=stratos-waybar-hyprland-config
pkgver=1.0
pkgrel=9
pkgdesc="Waybar configuration for StratOS' Hyprland spin"
# provides=('stratos-waybar-hyprland-config' 'stratos-waybar-niri-config')
arch=('any')
license=('GPL3')
depends=(
    'waybar'
    'ttf-jetbrains-mono-nerd'
)
source=()
optdepends=('ttf-jetbrains-mono-nerd: Default nerd font')
install=stratos-waybar-hyprland-config.install
prepare() {
    cp -r "$startdir"/.config/ "$srcdir"/
    cp -r "$startdir"/usr/local/bin/ "$srcdir"/
}
package() {
    install -d "$pkgdir"/etc/skel/.config
    cp -r "$srcdir"/.config/waybar/ "$pkgdir"/etc/skel/.config/
    
    install -d "$pkgdir/usr/local/bin"
    cp -a "$srcdir"/bin/* "$pkgdir"/usr/local/bin/
}
