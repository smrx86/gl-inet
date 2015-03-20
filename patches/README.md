Patches for GL-inet Buildroot / Build system
============================================
[smrx86][] project

The following patches split based on version /category:
(i assume your builtroot directory is /home/username/openwrt)

Attitude Adjustment 12.09
-------------------------
* **01-gl-inetAA16MiB.patch**, a patches for attitude adjustment 12.09 builroot. it make change to apply 16 MiB in f/w cooking process.

	howto use:

    $sudo apt-get install quilt
    
    $cat > ~/.quiltrc <<EOF
    
     QUILT_DIFF_ARGS="--no-timestamps --no-index -pab --color=auto"
     
     QUILT_REFRESH_ARGS="--no-timestamps --no-index -pab"
     
     QUILT_PATCH_OPTS="--unified"
     
     QUILT_DIFF_OPTS="-p"
     
     EDITOR="nano"
     
     EOF
     
    $cd openwrt
    
    $cat > patches/series <<EOF
    
     01-gl-inetAA16MiB.patch
     
     EOF
     
    $quilt push -a


Barrier Breaker 14.07
---------------------
* **02-gl_inetBB16MiB.patch**, a patches for barrier breaker 14.07 builroot. it make change to apply 16 MiB in f/w cooking process.

	howto use:

    $sudo apt-get install quilt
    
    $cat > ~/.quiltrc <<EOF
    
     QUILT_DIFF_ARGS="--no-timestamps --no-index -pab --color=auto"
     
     QUILT_REFRESH_ARGS="--no-timestamps --no-index -pab"
     
     QUILT_PATCH_OPTS="--unified"
     
     QUILT_DIFF_OPTS="-p"
     
     EDITOR="nano"
     
     EOF
     
    $cd openwrt
    
    $cat > patches/series <<EOF
    
     02-gl_inetBB16MiB.patch
     
     EOF
     
    $quilt push -a


* **130-mips_remove_plat_dma_functions.patch**, a patches for Barrier breaker buildroot. you can find the the origin trunk/target/linux/generic/patches-3.10. replace the origin with this patches.
(i your builtroot directory is /home/trunk)

	howto use:

    $cd trunk
    
    $cp 130-mips_remove_plat_dma_functions.patch /home/username/openwrt/target/linux/generic/patches-3.10

* **609-MIPS-ath79-ap136-fixes.patch**, a patches for Barrier breaker buildroot. you can find the the origin trunk/target/linux/generic/patches-3.10. replace the origin with this patches.

	howto use:

    $cd trunk
    
    $cp 609-MIPS-ath79-ap136-fixes.patc /home/username/openwrt/target/linux/generic/patches-3.10


[smrx86]: https://twitter.com/smrx86
