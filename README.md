<div id="toc">
  <ul style="list-style: none">
    <summary>
      <h1>USB Dolphin Docs</h1>
    </summary>
  </ul>
</div>

A USB 2.0 to EXI adapter for SP1 or Slot A/B of the GameCube.

Once available you can buy one here:  https://store.makstech.io/usb-dolphin
#
## Support
If you encounter any issues or have questions, join the [Discord server](https://discord.gg/YtA9aU3BKZ) for support.

## Firmware Updates
Once a new firmware is available, the necessary files will appear under releases.

How to start the update process:
1. Download the latest fw.bin file
2. Copy the fw.bin file into the root directory of a FAT32 formatted USB stick or drive (exFAT will not work!)
3. Plug the USB stick/drive into the USB Dolphin
4. Turn on your GameCube
5. Press the button on the USB Dolphin using a paperclip or similar to start the firmware update
   1. The green LED will flash whilst the bootloader searches for a USB stick/drive
   2. Both green and red LEDs will flash whilst the update is in progress (~10 seconds)
7. Wait until the green light is constantly on
8. Restart the GameCube

## Compatible USB Ethernet Adapters
> [!TIP]
> If you need to buy an adapter the __RTL8153__ or __RTL8156__ chipset is recommended.

> [!WARNING]
> Depending on your network and mostly if you use a 100 Mbit/s adapter, you may experience stuttering in video sequences.\
> Consider using a 1 Gbit/s adapter or creating a dedicated VLAN.

The following tables show an incomplete list of compatible chipsets/products and their limitations when using them with USB Dolphin.\
Adapters with an integrated hub will not work independently of the chipset.

| Chipset | Manufacturer | Max Link Speed | Auto MDIX | Max Frame Size | Protocol
| :--- | :--- | :----: | :----: | :----: | :----: |
| RTL8153 | Realtek | 1 Gbit/s | ✅ | 2044 | CDC-ECM
| RTL8156 | Realtek | 2.5 Gbit/s | ✅ | 2044 | CDC-ECM
| AX88179 | ASIX | 1 Gbit/s | ✅ | 2044 | Vendor
| AX88179B | ASIX | 1 Gbit/s | ✅ | 2040 | CDC-ECM
| AX88772 | ASIX | 100 Mbit/s | ❌ | 1532 | Vendor
| AX88772A <br> AX88772B | ASIX | 100 Mbit/s | ✅ | 1532 | Vendor
| CH397 | WCH | 100 Mbit/s | ✅ | 2043 | CDC-ECM
| NX7202 | Naxiang Technology | 100 Mbit/s | ✅ | 1514 | CDC-ECM

| Chipset | Known Products
| :--- | :--- |
| RTL8153 | TP-Link UE300 <br> uni UNIAE01 (UA03) <br> uni UNICE01 (UA02) <br> Simplecom NU301
| RTL8156 | UGREEN USB 2.5G (C)
| AX88179 | Amazon Basics USB 3.0 __*__
| AX88179B | UGREEN USB 1G __*__ <br> D-Link DUB-1312 __*__
| AX88772 | Wii LAN Adapter
| AX88772A | Apple A1277

__*__ _Not clear if the product always uses this chipset_

Untested chipsets that will likely work: AX88179A, AX88772C, AX88772D, AX88772E\
Currently unsupported chipsets: AX88178A, AX88172A, DM9601

You can post the device info shown by [UsbTreeView](https://www.uwe-sieber.de/usbtreeview_e.html) on the [Discord server](https://discord.gg/YtA9aU3BKZ) to clarify if an adapter is compatible.

## Special Thanks
- [Silversteel](https://x.com/silverstee1) for the PCB and amazing SP1 case design and his help in general
- [Extrems](https://github.com/Extrems), [emukidid](https://github.com/emukidid) and everyone involved in creating Swiss
