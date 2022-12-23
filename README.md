# Proceed on your own RISK!

## WARNING
This is both a hardward and a software modification so screwing your board up is not my problem!

## MOD

This mod bring the TL-WR841N-v14 back to life, with some hardward/software modifications you can still be using the latest OpenWrt firmware on this router.

- #### Hardward Modifications:

  Upgrade the SPI Flash to 8MB/16MB
  
  Upgrade the RAM to 64MB DDR1
  
- #### Software Modifications:

  I have built the U-Boot from [source code](https://www.tp-link.com/us/support/download/tl-wr841n/v14/#GPL-Code) changing the target image to V13 so the bootloader will accept flashing the V13 firmware on the V14
  
  Building OpenWrt form source adding 16MB to the Device Tree 

#### RAM
- If you are willing to take the RISK and upgrade your ram make sure to flash the [64MB U-Boot](https://github.com/daoudeddy/openwrt-wr841n/releases/download/22.03.2/uboot-v14-mod-64MB-RAM.bin)

#### SPI
- If you are willing to upgrade the SPI Flash only without the ram make sure to flash the [32MB U-Boot](https://github.com/daoudeddy/openwrt-wr841n/releases/download/22.03.2/uboot-v14-mod-32MB-RAM.bin)
- For 8MB SPI Flash you need to flash the fimware provided by OpenWrt from [here](https://openwrt.org/toh/hwdata/tp-link/tp-link_tl-wr841n_v13)

- For 16MB SPI Flash you need to flash the custom OpenWrt firmware from the [release](https://github.com/daoudeddy/openwrt-wr841n/releases) page

#### FLASHING THE BOOTLOADER

- For the SPI Flash I've used a Wemos D1 Mini with [Wiprog](https://github.com/kutis96/wiprog) or you can use any other method to flash the bootloader, but make sure to verify it before your proceed to flashing the firmware
 
- The original bootloader is attached [here](https://github.com/daoudeddy/openwrt-wr841n/releases/download/22.03.2/uboot-v14-orig.bin) in case it didnt work for you

