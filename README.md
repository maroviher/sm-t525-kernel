### Stock kernel for SM-T525

		Removed a lot of stuff (nobody needs it in daily use):
		CONFIG_PRINTK, CONFIG_ELF_CORE, CONFIG_RD_BZIP2, CONFIG_RD_LZMA, CONFIG_DEBUG_BUGVERBOSE, 
		CONFIG_SEC_DEBUGs, CONFIG_ANDROID_LOGGER, CONFIG_EXT2_FS, CONFIG_EXT3_FS, CONFIG_DEBUG_INFO,
		CONFIG_DEBUG_INFO, CONFIG_DEBUG_MEMORY_INIT, CONFIG_DYNAMIC_DEBUG, CONFIG_DEBUG_USER
		Disable software CRCs (mmc/spi):   
		such a test
		dd if=/dev/block/mmcblk0 of=/dev/null bs=100000
		CRC on: 120Mb/s
		CRC off: 165Mb/s

### How to compile:
		#set the path to toolchain in build_kernel.sh
		./build_kernel.sh
		#TWRP flashable image build/boot.img
		#WiFi will not work. To fix: modify /system/build.prop, ro.securestorage.support=true - Change to false and reboot
