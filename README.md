![Screenshot](https://i.imgur.com/ysFnjRY.png)
      
# rEFInd-chalkboard
A simple monochrome theme for the rEFInd UEFI boot manager

[rEFInd](http://www.rodsbooks.com/refind/) is a boot manager for UEFI systems and scans for kernels & EFI at boot.

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed.

 2. Create a folder called `themes` inside it, if it doesn't already exist

 3. Clone this repository into the `themes` directory as `themes/rEFInd-chalkboard`.

 4. To enable the theme add `include themes/rEFInd-chalkboard/theme.conf` at the end of `refind.conf`.
    
Entries should be autodetected and shown with the proper icons.

Manual entry can be done via `menuentry` option.

Example:

```
menuentry "Windows" {
	icon /EFI/refind/themes/rEFInd-chalkboard/icons/os_windows.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}
```

Other examples are in the `refind.conf` file.

-------------------------------
rEFInd-chalkboard notes
-------------------------------

September 1, 2018: Initial release of rEFInd-chalkboard to DeviantArt.
- Chalkboard stock image: http://www.danieljenkinsacademy.com/chalkboard-backgrounds-free-download-pixelstalk-33/

September 16, 2018: Second release of rEFInd-chalkboard to DeviantArt.
- This release increases all icon sizes to improve overall clarity and viewing ease.
- It replaces all of the icons, adding many additional icons in the process.
- It replaces the selection icon image to fit in better with the theme.
- The hand drawn font was redrawn to make it much more readable.
- New screenshots were captured using my new VirtualBox test machine to allow for much improved sample screens.

December 30, 2018: rEFInd-chalkboard theme uploaded to github.

January 6, 2019: Added icons for Sparky Linux, added GameDrift and Lakka

March 30, 2019: Added icons for Pop OS and Pisi Linux

April 10, 2019: Added icons for Parrot Sec OS, PureOS, and Qubes OS

December 18, 2020: Added new function icons func_bootorder.png and func_install.png

March 3, 2021: Added icon for Garuda Linux

February 13,2024: Added haiku_loader.efi to enable launching the Haiku Operating System
The simplest way I have found to launch a Haiku desktop on a UEFI machine is to setup rEFInd on a USB drive as Partition 1, so it launches first, set the UEFI to launch UEFI USB devices first, and make sure I have a folder called Haiku under EFI with the file haiku_loader.efi I just updated. That will find any Haiku builds you have on your system, or at least it should. It doesn't always work, for one reason or another. But it's pretty darn good, and it's nice to have Haiku on the rEFInd menu at last! I launch from a USB drive because it holds several key applications that I may require in the event of an emergency, such as a complete system failure.
