# buildroot
This builds dahliaOS linux-based builds easily. As of 22:43 On June 13, this is only a base buildroot and lacks the dahlia-specific overlays.

# Usage
Use ```make menuconfig``` to configure the build settings, ```make linux-menuconfig``` to configure the Linux kernel, and ```make``` to compile the image, which can be found under ```output/images```. Files can be inserted into the image using the ```output/target``` directory.

#Easy Modification
To compile and run the base dahliaOS toolchain, use ```make&&qemu-system-x86_64 --enable-kvm -m 4096 -cdrom output/images/rootfs.iso9660&&cp output/images/rootfs.iso9660 output/images/rootfs.iso```

# Requirements
It is recommended to have at minumum an Ethernet connection (directly to router), a dual-core x86 CPU and at least 4GB of RAM when compiling. I personally reccomend a 4C/8T or better CPU with 16GB of RAM for optimal speeds. You will also need a decent amount of hard drive space, I reccomend around 50GB if you clear out the build directory often. It takes around 6 hours to build a full image from scratch on a Dell Optiplex 790 with a 3GHZ i5-2400 and 16GB of RAM. I am sure a Threadripper or a newer Xeon CPU could easily handle compiling.

# Warning:
If you are using a laptop, make sure that you are aware of its temperature, some laptops easily heat up to 93-100c when compiling.
