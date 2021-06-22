# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>

pkgname=kernel-alive-openrc
_clean=linux-module-cleanup
pkgver=0.3
pkgrel=3
pkgdesc="Back up modules of current kernel to prevent some issues after kernel update"
url="https://github.com/shuryanc/kernel-alive-openrc-for-artix"
_commit=ceaf748126868e910c6bee7c288ffe86ad62457d
arch=(any)
license=(GPL3)
source=("$url/archive/$_commit.tar.gz")
depends=('rsync')
md5sums=('ef2fed216cd12f315892fddfa08bd25b')

package() {
	cd $pkgname-$_commit
	
#install systemd service
	install -Dm755 $_clean.script $pkgdir/usr/bin/$_clean
	install -Dm644 $_clean $pkgdir/etc/init.d/$_clean

#install hook and script	
	install -Dm644 $pkgname-pre.hook ${pkgdir}/usr/share/libalpm/hooks/$pkgname-pre.hook
	install -Dm644 $pkgname-post.hook ${pkgdir}/usr/share/libalpm/hooks/$pkgname-post.hook
	install -Dm644 $pkgname-install.hook ${pkgdir}/usr/share/libalpm/hooks/$pkgname-install.hook
	install -Dm644 $pkgname-remove.hook ${pkgdir}/usr/share/libalpm/hooks/$pkgname-remove.hook
	
	install -Dm755 $pkgname-pre.script ${pkgdir}/usr/share/libalpm/scripts/$pkgname-pre
	install -Dm755 $pkgname-post.script ${pkgdir}/usr/share/libalpm/scripts/$pkgname-post
	install -Dm755 $pkgname-remove.script ${pkgdir}/usr/share/libalpm/scripts/$pkgname-remove
}
