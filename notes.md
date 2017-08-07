Standard NVM Express Controller
-> BIOS device name
_SB.PCI0.RP09.PXSX


https://www.tonymacx86.com/threads/guide-dell-xps-15-9560-4k-touch-1tb-ssd-32gb-ram-100-adobergb.224486/
https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093/

    diskutil partitionDisk /dev/disk2 1 GPT HFS+J "install_osx" R


Download https://sourceforge.net/projects/cloverefiboot/files/latest/download

select the target of the install to "install_osx" using "Change Install Location"

select "Customize"
- check "Install for UEFI booting only", "Install Clover in the ESP" will automatically select
- check "BGM" from Themes (the config.plist files I provide use this theme)
- check "OsxAptioFixDrv-64" from Drivers64UEFI


sudo "/Applications/Install macOS Sierra.app/Contents/Resources/createinstallmedia" --volume  /Volumes/install_osx --applicationpath "/Applications/Install macOS Sierra.app" --nointeraction


 Copy attached Clover folder to the USB drive’s EFI partition

 Copy the Clover installer package to "Install OS X" partition

apply patches from https://raw.githubusercontent.com/RehabMan/patch-nvme/master/NVMe_patches_10_12_6.plist

<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#1</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>weAMBQAQAACJgw==</data>
  <key>Replace</key>
  <data>weAJBQAQAACJgw==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#2</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>D7aMiIIAAACD+QwPhTIBAA==</data>
  <key>Replace</key>
  <data>D7aMiIIAAACD+QkPhTIBAA==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#3</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>AMeDpAAAAAAQAABIi0gISA==</data>
  <key>Replace</key>
  <data>AMeDpAAAAAACAABIi0gISA==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#4</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>SYnGTYX2dGFBwecMSWP/vg==</data>
  <key>Replace</key>
  <data>SYnGTYX2dGFBwecJSWP/vg==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#5</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>hv8PAABIwegMD7cPgeH/Dw==</data>
  <key>Replace</key>
  <data>hv8PAABIwegJD7cPgeH/Dw==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#6_7</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>icGB4f8PAABIAdFIgfn/DwAAdzs=</data>
  <key>Replace</key>
  <data>icGB4f8BAABIAdFIgfn/AQAAdzs=</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#8</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>SYHF/w8AAEnB7QxJiwQkSA==</data>
  <key>Replace</key>
  <data>SYHF/w8AAEnB7QlJiwQkSA==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#9_10</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>BgIAAEyNuAAQAABMiflIgeEA8P//SYmGGgEAAEmJjiIBAABBvAAQAABJKfQ=</data>
  <key>Replace</key>
  <data>BgIAAEyNuAACAABMiflIgeEA8P//SYmGGgEAAEmJjiIBAABBvAACAABJKfQ=</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#11</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>AABJiY4iAQAAugAQAABIKQ==</data>
  <key>Replace</key>
  <data>AABJiY4iAQAAugACAABIKQ==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#12</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>yAAAAEkp17gAEAAATYskJA==</data>
  <key>Replace</key>
  <data>yAAAAEkp17gAAgAATYskJA==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#13</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>4b+AQBUGTYnWugAQAABFMQ==</data>
  <key>Replace</key>
  <data>4b+AQBUGTYnWugACAABFMQ==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#14</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>iWTY+EmBxAAQAABJgccA8A==</data>
  <key>Replace</key>
  <data>iWTY+EmBxAACAABJgccA8A==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#15</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>Bf8PAABIwegMZvfB/w8PlQ==</data>
  <key>Replace</key>
  <data>Bf8PAABIwegJZvfB/w8PlQ==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#16</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>weIIQQ+2wcHgDEQJ0EQJwA==</data>
  <key>Replace</key>
  <data>weIIQQ+2wcHgCUQJ0EQJwA==</data>
</dict>
<dict>
  <key>Comment</key>
  <string>IONVMeFamily Pike R. Alpha Patch#17</string>
  <key>Disabled</key>
  <false/>
  <key>Name</key>
  <string>IONVMeFamily</string>
  <key>Find</key>
  <data>RYTJD5XAD7bAweAMRAnYRA==</data>
  <key>Replace</key>
  <data>RYTJD5XAD7bAweAJRAnYRA==</data>
</dict>



** DIDNT WORK:

https://bitbucket.org/RehabMan/os-x-maciasl-patchmatic/downloads

// Inject bogus class-code for NVMe SSD to prevent IONVMeFamily.kext from loading
DefinitionBlock("", "SSDT", 2, "hack", "NVMe-Pcc", 0)
{
    External(_SB.PCI0.RP09.PXSX, DeviceObj)
    Method(_SB.PCI0.RP09.PXSX._DSM, 4)
    {
        If (!Arg2) { Return (Buffer() { 0x03 } ) }
        Return(Package()
        {
            "class-code", Buffer() { 0xff, 0x08, 0x01, 0x00 },
            "built-in", Buffer() { 0 },
        })
    }
}
//EOF

diskutil mount EFI

 --> save as SSDT-NVMe-Pcc.aml to CLOVER/ACPI/patched

 ./patch_nvme.sh --spoof 10_12_6
Copy HackrNVMeFamily-10_12_6.kext to CLOVER/kexts/Other
** --
