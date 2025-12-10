# - Bootlogos-SM8350-AC (1) -
> ⛔ : THIS PROJECT IS NOT FINISHED!!! (I think)
> 
> ⚠️ : If you are here just out of curiosity or you barely know how to install a ROM, you should not touch it.

This is the Bootlogos repository for the **Tundra**, better known as **Moto Edge 30 Fusion and S30 Pro** phone. That's all I can describe for a README. Now, let's move on to the bootlogo previews of the ROMs.

| LineageOS | AwakenOS | PixelOS (Style 1) | PixelOS (Style 2) |
| --- | --- | --- | --- |
| ![logo](https://image2url.com/images/1765338703163-f791601c-4c95-4ed8-8abc-5ef023c9e262.png) | ![logo](https://image2url.com/images/1765338740860-b0c69c71-6723-42bd-8b4d-fbe9ea60dcb1.png) | ![logo](https://image2url.com/images/1765338791858-3ec4cf98-96aa-4685-8c96-9dfb0eb8d083.png) | ![logo](https://image2url.com/images/1765338838431-f6611845-daf2-4479-a9e2-613c6c36726c.png) |

| PixelOS (Style 3) | PixelOS (Style 4) | Evolution X | HyperOS |
| --- | --- | --- | --- |
| ![logo](https://image2url.com/images/1765338885478-ba24eaf4-d71e-4c66-b97c-4d51fdece3a7.png) | ![logo](https://image2url.com/images/1765338920809-b6651fca-db09-4378-802d-38d984df6560.png) | ![logo](https://image2url.com/images/1765338967297-957885ca-159a-4df8-90fe-99dbdc10417d.png) | ![logo](https://image2url.com/images/1765339019227-b1035f40-127d-485d-87ec-d57f8aac5f92.png) |

# - Requirements -
- Unlocked Bootloader
- Root (For mobile method)
- PC or OTG with other phone (Use Bugjaeger)
- Android Platform Tools (with installed Motorola USB driver on Windows)

# - How to flash? (PC Method) -
1. Reboot the phone to fastboot/bootloader mode
2. Insert command to flash bootlogo
```bash
fastboot flash logo <path/to/logo.bin>
```
3. Reboot the phone

# - How to flash? (Mobile Method) -
1. Download and install the ReTermimal
[Download Here](https://github.com/RohitKushvaha01/ReTerminal/releases) - Credits to [RohitKushvaha01](https://github.com/RohitKushvaha01)
3. Open it until you reach this screen:
<img width="400" alt="Screenshot_20251201-041431_ReTerminal" src="https://github.com/user-attachments/assets/bbb805c9-8b86-47e3-bbd0-975322c381a6" />

4. Click on "+" and then "Android"
<img width="400" alt="Screenshot_20251201-041437_ReTerminal" src="https://github.com/user-attachments/assets/d92f2a15-023a-4ab0-b178-3e3ef9e537ac" />

5. Insert command
```bash
su
```
> (Note: if you are in Magisk, it will ask you on your screen, but if you are in APatch/KernelSU, you have to open the root manager, superuser and activate ReTerminal for the super user to be active)

5. Enter the directory where the downloaded logo.bin is located, using cd
 ```bash
cd <path/to/directory>
```
> For example, if your downloaded logo.bin is in the "Download" folder of the internal storage, enter the command
```bash
cd /storage/emulated/0/Download
```
6. Insert command to flash a bootlogo
```bash
dd if=<logo>.bin of=/dev/block/by-name/logo_<current slot> bs=16777216
```
7. Reboot the phone and you will see the new bootlogo!
