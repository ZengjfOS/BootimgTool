# BootimgTool

用于`Android 4.2`的`boot.img`的分解、合成。

## unpacking boot.img

* 替换当前目录下的`boot.img`；
* 执行：`./split_boot boot.img`；
* 在当前目录下会生成一个`boot`目录：
```
    .(boot)
    ├── boot.img-kernel
    ├── boot.img-ramdisk.cpio.gz
    └── ramdisk
        ├── data
        ├── default.prop
        ├── dev
        ├── fstab.freescale
        ├── init
        ├── init.freescale.rc
        ├── init.freescale.usb.rc
        ├── init.goldfish.rc
        ├── init.rc
        ├── init.trace.rc
        ├── init.usb.rc
        ├── proc
        ├── sbin
        │   ├── adbd
        │   ├── ueventd -> ../init
        │   └── watchdogd -> ../init
        ├── sys
        ├── system
        ├── ueventd.freescale.rc
        ├── ueventd.goldfish.rc
        └── ueventd.rc

    7 directories, 17 files
```

## repacking boot.img

* 基于前面的《unpacking boot.img》一小节才能运行后续命令；
* 运行命令：`./repack`；
* 将在当前目录看到：`newboot.img`。
