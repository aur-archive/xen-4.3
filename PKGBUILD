# Maintainer: David Sutton <kantras - gmail.com>
# Contributor: Shanmu Thiagaraja <sthiagaraja+AUR@prshanmu.com>
# Contributor: Limao Luo
# Contributor: Luceo
# Contributor: Revellion

pkgname=xen-4.3
_pkgname=xen
pkgver=4.3.3
pkgrel=1
pkgdesc="Virtual Machine Hypervisor & Tools - v4.3"
arch=(i686 x86_64)
url="http://www.xenproject.org/"
license=(GPL2)
depends=(bin86 bluez bridge-utils curl e2fsprogs gnutls iproute2 libaio libcap-ng libiscsi libjpeg-turbo libpng libseccomp lzo2 nss pixman pciutils python python2 sdl wget vde2 yajl)
[[ "$CARCH" == "x86_64" ]] && depends+=(lib32-glibc)
makedepends=(cmake dev86 git iasl markdown ocaml-findlib)
optdepends=('xen-docs: Official Xen Documentation' 'openvswitch: Optional Networking support')
conflicts=(xen-4.2{,-testing-hg} xen-{gdbsx,hg-unstable,rc,git} xen xen-4.4)
backup=(etc/$_pkgname/xend-{config,pci-{permissive,quirks}}.sxp etc/modules-load.d/$_pkgname.conf etc/$_pkgname/xl.conf etc/conf.d/xen{stored,consoled,domains} etc/default/xencommons etc/$_pkgname/grub.conf)
options=(!buildflags !strip)
provides=('xen')
install=xen.install
changelog=ChangeLog
source=(http://bits.xensource.com/oss-xen/release/$pkgver/xen-$pkgver.tar.gz
    http://xenbits.xen.org/xen-extfiles/ipxe-git-9a93db3f0947484e30e753bbd61a10b17336e20e.tar.gz
    http://xenbits.xen.org/xen-extfiles/lwip-1.3.0.tar.gz
    http://xenbits.xen.org/xen-extfiles/zlib-1.2.3.tar.gz
    http://xenbits.xen.org/xen-extfiles/newlib-1.16.0.tar.gz
    http://xenbits.xen.org/xen-extfiles/pciutils-2.2.9.tar.bz2
    http://xenbits.xen.org/xen-extfiles/polarssl-1.1.4-gpl.tgz
    http://xenbits.xen.org/xen-extfiles/grub-0.97.tar.gz
    http://xenbits.xen.org/xen-extfiles/tpm_emulator-0.7.4.tar.gz
    http://xenbits.xen.org/xen-extfiles/gmp-4.3.2.tar.bz2
    xen.install
    09_xen
    localgcc490fix.patch
    bios_workaround.patch
    xendomains.patch
    TOM-register.patch
    ati-passthrough.patch
    IVRS-debug.patch
    xsa104.patch
    xsa105.patch
    xsa106.patch
    xsa108.patch
    proc-xen.mount
    var-lib-xenstored.mount
    xenconsoled.service
    conf.d-xenconsoled
    xendomains.service
    xendomU@.service
    xenstored.service
    conf.d-xenstored
    tmpfiles.d-xen.conf
    grub.conf
    xen.conf)
noextract=(lwip-1.3.0.tar.gz
    zlib-1.2.3.tar.gz
    newlib-1.16.0.tar.gz
    pciutils-2.2.9.tar.bz2
    polarssl-1.1.4-gpl.tgz
    grub-0.97.tar.gz
    tpm_emulator-0.7.4.tar.gz
    gmp-4.3.2.tar.bz2
    ipxe-git-9a93db3f0947484e30e753bbd61a10b17336e20e.tar.gz)

sha256sums=('59eb0e1c4a1f66965fe56dcf27cdb5872bf7e0585b7f2e60bd7967ec7f744ebf'
            '632ce8c193ccacc3012bd354bdb733a4be126f7c098e111930aa41dad537405c'
            '772e4d550e07826665ed0528c071dd5404ef7dbe1825a38c8adbc2a00bca948f'
            '1795c7d067a43174113fdf03447532f373e1c6c57c08d61d9e4e9be5e244b05e'
            'db426394965c48c1d29023e1cc6d965ea6b9a9035d8a849be2750ca4659a3d07'
            'f60ae61cfbd5da1d849d0beaa21f593c38dac9359f0b3ddc612f447408265b24'
            '2d29fd04a0d0ba29dae6bd29fb418944c08d3916665dcca74afb297ef37584b6'
            '4e1d15d12dbd3e9208111d6b806ad5a9857ca8850c47877d36575b904559260b'
            '4e48ea0d83dd9441cc1af04ab18cd6c961b9fa54d5cbf2c2feee038988dea459'
            '936162c0312886c21581002b79932829aa048cfaf9937c6265aeaa14f1cd1775'
            '2d0d342fd03109f52521334f6ffda2681f60d5002c8ac0323dd466eea3c1a912'
            '06c9f6140f7ef4ccfc4b1a7d9732a673313e269733180f53afcd9e43bf6c26bb'
            '090748012bc8f34fceaa235a949a48bf997c208738d9f3b7aa7ffebbf103a010'
            '914cc983da1fe89ff125d751c979b4968f8952da21b19b900fcd4e6b33e14552'
            '1938ca36bfb62c76ad0642147017ecfaa64588abaa2d88e868f501c4ae83bfd9'
            '0fa9426cc499ea3d6e1aa33a8be0e180aed87936814b9b88bb0ef42f6983654a'
            'd93c2d5bcdf0c3e4c6e8efb357cb4b9d618209025361f5ccd9d03651a8acd7a3'
            '54883171ff9cf5f342a2be5c944df16902ef06b6f2d015b675fa9bd5ed899c7c'
            'fc02f6365ca79a6ef386c882b57fab8b56aa12b54fc9b05054552f0f25e32047'
            'dfb5ede7cc5609a812a7b1239479cefd387f9f9c8c25e11e64199bc592ad7e39'
            '301060f801ab39c15ac773e1bcc250f0e6bf30d748007a96173459b83afc9270'
            'cf7ecf4b4680c09e8b1f03980d8350a0e1e7eb03060031788f972e0d4d47203e'
            '139eed988bfaf8edc8ccdfd0b668382bd63db48ce17be91776182a7e28e9d88c'
            'c19146931c6ab8e53092bd9b2ebbfda5c76fd22ad3b1d42dcda3dd1b61f123ff'
            'e4af7891e816b9549ebeff766a78036626c0e278734e5625b8e7d68729530ded'
            '48d76cc6f25caa79b3f527c96a0883b1decb9012f6616f61336c8d43791bf007'
            '0bd45d9de6456c4f9adf32e726f2db3a3cd0423c1d161b442e8a1666d2e68e3f'
            '012cc60ffdcb0e061d04d404eb9232734554aef4dc4b551f66adf82a655e6e41'
            '8ee5c5a14064fc2bbfd38d0ec8a6001f541bbe56b9fb534733209a8af148b297'
            '0e1ad0a6a72b0c22025a556c23235a8f663427f1e769c45fe39d1c525bf82eff'
            '40e0760810a49f925f2ae9f986940b40eba477dc6d3e83a78baaae096513b3cf'
            '3f0af16958c3e057b9baa5afc47050d9adf7dd553274dd97ae4f35938fefb568'
            '50a9b7fd19e8beb1dea09755f07318f36be0b7ec53d3c9e74f3266a63e682c0c')

prepare() {
    cd $_pkgname-$pkgver/

    ### Security Patches
    patch -Np1 -i $srcdir/xsa104.patch
    patch -Np1 -i $srcdir/xsa105.patch
    patch -Np1 -i $srcdir/xsa106.patch
    patch -Np1 -i $srcdir/xsa108.patch

    ### Compile Patches
    patch -Np1 -i $srcdir/localgcc490fix.patch

    ### Functionality Patches
    patch -Np1 -i $srcdir/TOM-register.patch

    # Uncomment line below if you have a bios which is reporting bad IVRS data
    #patch -Np1 -i $srcdir/bios_workaround.patch
    #patch -Np1 -i $srcdir/IVRS-debug.patch

    # Uncomment line below if you want to enable ATI Passthrough support (some reported successes)
    #patch -Np1 -i $srcdir/ati-passthrough.patch

    ### Distribution Patching
    patch -Np1 -i $srcdir/xendomains.patch

    # Fix Install Paths
    sed -i 's:/sbin:/bin:' config/StdGNU.mk

    # Bypass distribution auto-discovery
    echo "CONFIG_LEAF_DIR=default" >> .config
    echo "SUBSYS_DIR=/run" >> .config
    echo "INITD_DIR=/etc/init.d" >> .config

    # Copy supporting tarballs into place
    cp $srcdir/lwip-1.3.0.tar.gz stubdom/
    cp $srcdir/zlib-1.2.3.tar.gz stubdom/
    cp $srcdir/newlib-1.16.0.tar.gz stubdom/
    cp $srcdir/pciutils-2.2.9.tar.bz2 stubdom/
    cp $srcdir/polarssl-1.1.4-gpl.tgz stubdom/
    cp $srcdir/grub-0.97.tar.gz stubdom/
    cp $srcdir/tpm_emulator-0.7.4.tar.gz stubdom/
    cp $srcdir/gmp-4.3.2.tar.bz2 stubdom/

}

build() {
    export CFLAGS+='-Wall -Wstrict-prototypes -Wno-unused-local-typedefs -Wno-sizeof-pointer-memaccess'
    cd $_pkgname-$pkgver/
    ./autogen.sh
    ./configure PYTHON=/usr/bin/python2 --prefix=/usr --localstatedir=/run
    unset CFLAGS
}

package() {
    cd $_pkgname-$pkgver/

    make DESTDIR="$pkgdir" LANG=C PYTHON=python2 install-{xen,tools,stubdom}

    # Install files from AUR package
    cd ../
    for f in ${source[@]}; do
        [[ $f =~ .mount || $f =~ .service ]] && install -Dm644 $f "$pkgdir"/usr/lib/systemd/system/$f
    done
    install -Dm644 tmpfiles.d-$_pkgname.conf "$pkgdir"/usr/lib/tmpfiles.d/$_pkgname.conf

    install -Dm644 $_pkgname.conf "$pkgdir"/etc/modules-load.d/$_pkgname.conf
    install -Dm644 conf.d-xenstored "$pkgdir"/etc/conf.d/xenstored
    install -Dm644 conf.d-xenconsoled "$pkgdir"/etc/conf.d/xenconsoled
    install -Dm644 grub.conf "$pkgdir"/etc/xen/grub.conf
    install -Dm755 09_xen "$pkgdir"/etc/grub.d/09_xen

    cd "$pkgdir"

    # Fix paths in scripts, move to right locations and create missing directories
    sed -i 's:/var/lock:/run/lock:' etc/init.d/xendomains
    sed -i 's:/var/lock:/run/lock:' etc/init.d/xend
    sed -i 's:/var/lock:/run/lock:' etc/xen/scripts/hotplugpath.sh
    sed -i 's:/var/run:/run:' etc/xen/scripts/hotplugpath.sh
    mv etc/{init,rc}.d
    mv etc/rc.d/xendomains etc/xen/scripts/xendomains
    mv etc/default/xendomains etc/conf.d/xendomains
    mv var/xen/dump var/lib/xen/
    mkdir var/log/xen/console

    # Sanitize library path (if lib64 exists)
    if [[ -d usr/lib64 ]]; then
        cd usr/
        cp -r lib64/* lib/
        rm -rf lib64
	cd ../
    fi

    # Compress and move syms file to a different directory
    gzip boot/$_pkgname-syms-$pkgver
    mv boot/$_pkgname-syms-$pkgver.gz usr/share/xen

    ##### Kill unwanted stuff #####
    # hypervisor symlinks
    rm -f boot/xen{,-4,-4.3}.gz

    # Documentation cleanup ( see xen-docs package )
    rm -rf usr/share/doc
    rm -rf usr/share/xen/man

    # Pointless helper cleanup
    rm -f usr/bin/xen-python-path
    rm -rf usr/libexec

    # Unnecessary qemu support files
    rm -rf usr/bin/qemu-*-xen
    rm usr/share/qemu-xen/qemu/{palcode,openbios}-*
    rm usr/share/xen/qemu/openbios-*

    # Clean up udev rules naming, remove depreciated xend.rules
    mv etc/udev/rules.d/xen-backend.rules etc/udev/rules.d/40-xen-backend.rules
    rm etc/udev/rules.d/xend.rules

    # Clean up left over empty directories
    rm -rf var/run var/lock var/xen

    # adhere to Static Library Packaging Guidelines
    rm -rf usr/lib/*.a
}
