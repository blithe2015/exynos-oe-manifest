# exynos-oe-manifest

## How to do

```
1.repo init -u https://github.com/blithe2015/exynos-oe-manifest.git -b main
2.repo sync -j$(nproc)
```

## Use Yocto

1. . layers/openembedded-core/oe-init-build-env
2. bitbake-layers add-layer $BUILDDIR/../layers/meta-exynos
3. vim $BUILDDIR/conf/local.conf<br>
    `# MCHINE ??= "qemux86-64"`<br>
    `MACHINE ??= "exynos"`<br>
4. image<br>
bitbake core-image-full-cmdline<br>
5. SDK<br>
bitbake core-image-full-cmdline -c populate_sdk
